<template>
  <div>
    <NavBar :navAdminMode="navAdminMode" />
    <div id="gpMain" class="gp-main">
      <div id="gpLoginBox" class="gp-login-box">
        <div class="gp-login-header">Sign In</div>
        <div class="gp-login-slogan">Please enter your credentials</div>
        
        <div id="gpLogInForm" class="gp-login-form">
          <input id="gpLoginUsername" type="text" class="gp-login-input" placeholder="Username" />
          <input id="gpLoginPassword" type="password" class="gp-login-input" placeholder="Password" />
          
          <div id="gpLogInMessage" class="gp-login-message gp-hidden"></div>
          
          <div id="gpLogInActions" class="gp-login-actions">
            <button id="gpLoginOK" class="gp-login-action gp-login-ok">Login</button>
          </div>
        </div>
      </div>
    </div>
    <Cookies />
    <Copyright />
  </div>
</template>

<script setup lang="ts">
import { useSeoMeta, useHead } from "@vueuse/head";
import { useRouter } from "vue-router";
import { onMounted } from "vue";

const title = "Golem Protocol | Login";
const description = "Sign in to Golem Protocol";

useSeoMeta({
  title: () => title,
  description: () => description,
  charset: "utf-8",
  viewport: "width=device-width, initial-scale=1.0",
});

useHead({
  link: [
    { rel: "icon", type: "image/png", href: "/logo.png" },
    { rel: "stylesheet", href: "/reset.css" },
    { rel: "stylesheet", href: "/custom.css" },
  ],
});

// Cookies
const allowCookies = useCookie<boolean>("allowCookies", {
  sameSite: "none",
  secure: true,
  maxAge: 60 * 60 * 24,
});
allowCookies.value = allowCookies.value ?? false;

const retries = useCookie<number>("retries", {
  sameSite: "none",
  secure: true,
  maxAge: 60 * 60,
});
retries.value = retries.value ?? 0;

const username = useCookie<string>("username", {
  sameSite: "none",
  secure: true,
  maxAge: 60 * 60 * 24,
});
username.value = username.value ?? "";

const accessToken = useCookie<string>("accessToken", {
  sameSite: "none",
  secure: true,
  maxAge: 60 * 60 * 24,
});
accessToken.value = accessToken.value ?? "";

const userLevel = useCookie<number>("userLevel", {
  sameSite: "none",
  secure: true,
  maxAge: 60 * 60 * 24,
});
userLevel.value = userLevel.value ?? -1;

const fullName = useCookie<string>("fullName", {
  sameSite: "none",
  secure: true,
  maxAge: 60 * 60 * 24,
});
fullName.value = fullName.value ?? "";

const router = useRouter();
let navAdminMode = userLevel.value >= 2 ? "gp-nav-admin" : "";
const gpServer = "https://golem-protocol-api.vercel.app";

type AuthResponse = {
  accessToken: string;
  userLevel: number;
  fullName: string;
  message: string;
};

let isLoggedIn = false;

// Check if already logged in
if (accessToken.value && accessToken.value !== "") {
  isLoggedIn = true;
  if (userLevel.value <= 1) {
    router.push("/");
  } else if (userLevel.value >= 2) {
    router.push("/admin");
  }
}

// Setup login form
onMounted(() => {
  // If already logged in, don't show form
  if (isLoggedIn) return;
  
  const loginBox = document.getElementById("gpLoginBox") as HTMLDivElement;
  const loginUsername = document.getElementById("gpLoginUsername") as HTMLInputElement;
  const loginPassword = document.getElementById("gpLoginPassword") as HTMLInputElement;
  const loginMessage = document.getElementById("gpLogInMessage") as HTMLDivElement;
  const loginOK = document.getElementById("gpLoginOK") as HTMLButtonElement;
  
  if (!loginBox || !loginUsername || !loginPassword || !loginMessage || !loginOK) {
    console.error("Missing login elements");
    return;
  }
  
  // Show the login box
  loginBox.style.display = "block";
  
  // Check retries
  if (retries.value >= 3) {
    loginMessage.innerText = "Too many attempts, try again after 1 hour.";
    loginMessage.classList.remove("gp-hidden");
    loginOK.disabled = true;
    return;
  }
  
  // Login button click handler
  loginOK.onclick = async () => {
    const tempUsername = loginUsername.value.trim();
    const tempPassword = loginPassword.value;
    
    // Clear previous message
    loginMessage.classList.add("gp-hidden");
    loginMessage.innerText = "";
    
    // Validation
    if (!tempUsername) {
      loginMessage.innerText = "Username is required.";
      loginMessage.classList.remove("gp-hidden");
      return;
    }
    
    if (!tempPassword) {
      loginMessage.innerText = "Password is required.";
      loginMessage.classList.remove("gp-hidden");
      return;
    }
    
    // Disable inputs during login
    loginUsername.disabled = true;
    loginPassword.disabled = true;
    loginOK.disabled = true;
    loginOK.textContent = "Logging in...";
    
    try {
      const response = await $fetch<AuthResponse>(`${gpServer}/authorize`, {
        method: "POST",
        headers: { "Content-Type": "application/json" },
        body: {
          username: tempUsername,
          password: tempPassword,
        }
      });
      
      if (response.accessToken && response.accessToken !== "") {
        // Save to cookies
        accessToken.value = response.accessToken;
        userLevel.value = response.userLevel;
        fullName.value = response.fullName;
        username.value = tempUsername;
        
        // Reset retries on successful login
        retries.value = 0;
        
        // Redirect based on user level
        if (response.userLevel <= 1) {
          router.push("/");
        } else {
          router.push("/admin");
        }
      } else {
        // Failed login
        retries.value = (retries.value || 0) + 1;
        loginMessage.innerText = response.message || "Invalid username or password";
        loginMessage.classList.remove("gp-hidden");
        
        // Re-enable inputs
        loginUsername.disabled = false;
        loginPassword.disabled = false;
        loginOK.disabled = false;
        loginOK.textContent = "Login";
        
        // Clear password field
        loginPassword.value = "";
      }
    } catch (error: any) {
      console.error("Login error:", error);
      loginMessage.innerText = "Connection error. Please try again.";
      loginMessage.classList.remove("gp-hidden");
      
      // Re-enable inputs
      loginUsername.disabled = false;
      loginPassword.disabled = false;
      loginOK.disabled = false;
      loginOK.textContent = "Login";
    }
  };
  
  // Enter key support
  loginPassword.onkeypress = (e) => {
    if (e.key === "Enter") {
      loginOK.click();
    }
  };
  
  loginUsername.onkeypress = (e) => {
    if (e.key === "Enter") {
      loginPassword.focus();
    }
  };
});
</script>

<style scoped>
.gp-login-box {
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 340px;
  padding: 30px;
  background: white;
  border-radius: 12px;
  box-shadow: 0 10px 40px rgba(0, 0, 0, 0.2);
  z-index: 1000;
}

.gp-login-header {
  font-size: 1.8em;
  font-weight: bold;
  text-align: center;
  margin-bottom: 10px;
  color: #333;
}

.gp-login-slogan {
  text-align: center;
  color: #666;
  margin-bottom: 30px;
  font-size: 0.9em;
}

.gp-login-form {
  display: flex;
  flex-direction: column;
  gap: 15px;
}

.gp-login-input {
  padding: 12px;
  font-size: 1em;
  border: 1px solid #ddd;
  border-radius: 6px;
  outline: none;
  transition: border-color 0.3s;
}

.gp-login-input:focus {
  border-color: #3f7d58;
}

.gp-login-message {
  padding: 10px;
  background: #fee;
  border: 1px solid #fcc;
  border-radius: 6px;
  color: #c33;
  font-size: 0.85em;
  text-align: center;
}

.gp-login-actions {
  margin-top: 10px;
}

.gp-login-action {
  width: 100%;
  padding: 12px;
  font-size: 1em;
  font-weight: bold;
  border: none;
  border-radius: 6px;
  cursor: pointer;
  transition: background-color 0.3s;
}

.gp-login-ok {
  background: #3f7d58;
  color: white;
}

.gp-login-ok:hover {
  background: #2e5a40;
}

.gp-login-ok:disabled {
  background: #ccc;
  cursor: not-allowed;
}

.gp-hidden {
  display: none !important;
}
</style>