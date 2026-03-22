<script lang="ts"></script>

<template>
  <client-only>
    <NavBar :navAdminMode="navAdminMode" />
    <div id="gpMain" class="gp-main">
      
      <div id="gpLoginBox" class="gp-login-box gp-hidden">
        <div class="gp-login-header">Sign In</div>
        <div class="gp-login-slogan">Please enter your credentials</div>
        
        <div id="gpLogInForm" class="gp-login-form">
          <input id="gpLoginUsername" type="text" class="gp-login-input" placeholder="Username" />
          <input id="gpLoginPassword" type="password" class="gp-login-input" placeholder="Password" />
          
          <div id="gpLogInMessage" class="gp-login-message gp-hidden"></div>
          
          <div id="gpLogInActions" class="gp-login-actions">
            <div id="gpLoginOK" class="gp-login-action gp-login-ok" data-busy="0">Login</div>
          </div>
        </div>
      </div>

    </div>
    <Cookies />
    <Copyright />
  </client-only>
</template>

<script setup lang="ts">
import { useSeoMeta, useHead } from "@vueuse/head";

const title = "Golem Protocol | Login";
const description = "An API Platform Library";

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
    { rel: "preconnect", href: "https://fonts.googleapis.com" },
    { rel: "preconnect", href: "https://fonts.gstatic.com", crossorigin: "" },
    { rel: "stylesheet", href: "https://fonts.googleapis.com/xxx" },
  ],
});

const globalDelay = 500;
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

function getByID<T extends HTMLElement>(id: string) {
  return document.getElementById(id) as T;
}

let lastLoginClicked = 0;

function checkAuthorizations() {
  console.log("checkAuthorizations called");
  
  // Check if user is already logged in (has token)
  if (accessToken.value && accessToken.value !== "") {
    console.log("Has token, redirecting to:", userLevel.value <= 1 ? "/" : "/admin");
    if (userLevel.value <= 1) {
      router.push("/");
    } else if (userLevel.value >= 2) {
      router.push("/admin");
    }
    return;
  }

  // If no token, show the login form
  console.log("No token, showing login form");
  
  const loginBox = document.getElementById("gpLoginBox") as HTMLDivElement;
  const loginForm = document.getElementById("gpLogInForm") as HTMLDivElement;
  const loginUsername = document.getElementById("gpLoginUsername") as HTMLInputElement;
  const loginPassword = document.getElementById("gpLoginPassword") as HTMLInputElement;
  const loginMessage = document.getElementById("gpLogInMessage") as HTMLDivElement;
  const logInActions = document.getElementById("gpLogInActions") as HTMLDivElement;
  const loginOK = document.getElementById("gpLoginOK") as HTMLDivElement;

  if (
    !loginBox ||
    !loginForm ||
    !loginUsername ||
    !loginPassword ||
    !loginMessage ||
    !logInActions ||
    !loginOK
  ) {
    console.log("Missing DOM elements");
    return;
  }

  if (retries.value >= 3) {
    loginForm.classList.add("gp-hidden");
    loginMessage.classList.remove("gp-hidden");
    loginMessage.innerText = "Too many attempts, try again after 1 hour.";
    logInActions.classList.add("gp-hidden");
    return;
  }

  // Set busy flag directly on the element
  loginOK.setAttribute("data-busy", "0");
  loginBox.classList.remove("gp-hidden");

  // Remove existing listeners by replacing with clone
  const newLoginOK = loginOK.cloneNode(true) as HTMLDivElement;
  loginOK.parentNode?.replaceChild(newLoginOK, loginOK);

  // Add click listener to the new button
  newLoginOK.addEventListener("click", () => {
    const isBusy = newLoginOK.getAttribute("data-busy");
    if (isBusy === "1") return;

    const tempUsername = loginUsername.value;
    const tempPassword = loginPassword.value;

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

    authorizeEmail(tempUsername, tempPassword);
  });

  loginUsername.addEventListener("keyup", (e) => {
    if (e.key === "Enter" && loginUsername.value) {
      loginPassword.focus();
    }
  });

  loginPassword.addEventListener("keyup", (e) => {
    if (e.key === "Enter") {
      const btn = document.getElementById("gpLoginOK") as HTMLDivElement;
      if (btn) btn.click();
    }
  });

  loadModal();
}

async function authorizeEmail(tempUsername: string, tempPassword: string) {
  if (lastLoginClicked >= Date.now() - globalDelay) return;
  lastLoginClicked = Date.now();

  const loginUsername = document.getElementById("gpLoginUsername") as HTMLInputElement;
  const loginPassword = document.getElementById("gpLoginPassword") as HTMLInputElement;
  const loginMessage = document.getElementById("gpLogInMessage") as HTMLDivElement;
  const loginOK = document.getElementById("gpLoginOK") as HTMLDivElement;

  if (!loginUsername || !loginPassword || !loginOK || !loginMessage) return;

  loginMessage.innerText = "";
  loginMessage.classList.add("gp-hidden");
  loginUsername.disabled = true;
  loginPassword.disabled = true;
  loginOK.setAttribute("data-busy", "1");

  try {
    userLevel.value = -1;

    const response = (await $fetch(`${gpServer}/authorize`, {
      headers: { "Content-Type": "application/json" },
      method: "POST",
      body: {
        username: tempUsername,
        password: tempPassword,
      }
    })) as AuthResponse;

    console.log("Login response:", response);

    accessToken.value = String(response.accessToken);
    userLevel.value = Number(response.userLevel);
    fullName.value = String(response.fullName);

    if (accessToken.value) {
      username.value = tempUsername;
      console.log("Login successful! Token set:", accessToken.value);
      
      // Small delay to ensure cookies are saved before redirect
      setTimeout(() => {
        if (userLevel.value <= 1) {
          router.push("/");
        } else if (userLevel.value >= 2) {
          router.push("/admin");
        }
      }, 100);
    }

    loginOK.setAttribute("data-busy", "0");

    if (!accessToken.value) {
      retries.value = (retries.value || 0) + 1;
    }

    if (response.message) {
      loginMessage.innerText = response.message;
      loginMessage.classList.remove("gp-hidden");
    }
  } catch (e: any) {
    console.error("Login error:", e);
    loginMessage.innerText = `Error encountered: ${e}`;
    loginMessage.classList.remove("gp-hidden");
    loginOK.setAttribute("data-busy", "0");
  }

  loginUsername.disabled = false;
  loginPassword.disabled = false;
  loginUsername.value = "";
  loginPassword.value = "";
}

function loadModal() {
  const cookieModal = getByID<HTMLDivElement>("gpCookieModal");
  const cookieBox = getByID<HTMLDivElement>("gpCookieBox");
  const cookieX = getByID<HTMLDivElement>("gpCookieX");
  const cookieOK = getByID<HTMLDivElement>("gpCookieOK");

  if (!cookieModal || !cookieBox || !cookieX || !cookieOK) return;

  if (allowCookies.value === true) {
    allowAllCookies();
    return;
  }

  showCookiePopup();

  cookieX.addEventListener("click", () => {
    showCookiePopup(false);
  });

  cookieOK.addEventListener("click", () => {
    allowAllCookies();
  });
}

function showCookiePopup(show: boolean = true) {
  const cookieBox = getByID<HTMLDivElement>("gpCookieBox");
  const cookieModal = getByID<HTMLDivElement>("gpCookieModal");

  if (!cookieBox || !cookieModal) {
    setTimeout(showCookiePopup, 50);
    return;
  }

  if (!show) {
    cookieBox.classList.add("gp-hidden");
    cookieModal.classList.add("gp-hidden");
    return;
  }

  cookieBox.classList.remove("gp-hidden");
  cookieModal.classList.remove("gp-hidden");
}

let lastCookieClicked = 0;

function allowAllCookies() {
  if (lastCookieClicked >= Date.now() - globalDelay) return;
  lastCookieClicked = Date.now();
  allowCookies.value = true;
  showCookiePopup(false);
}

onMounted(() => {
  console.log("=== Login Page Mounted ===");
  console.log("accessToken:", accessToken.value);
  console.log("userLevel:", userLevel.value);
  console.log("Cookies:", document.cookie);
  
  // Wait for DOM to be fully rendered
  nextTick(() => {
    console.log("Setting up login form...");
    
    // Get elements
    const loginBox = document.getElementById("gpLoginBox");
    const loginUsername = document.getElementById("gpLoginUsername") as HTMLInputElement;
    const loginPassword = document.getElementById("gpLoginPassword") as HTMLInputElement;
    const loginOK = document.getElementById("gpLoginOK");
    
    console.log("Login button found:", loginOK);
    
    // Manually attach click event if needed
    if (loginOK) {
      // Remove any existing listeners by cloning and replacing
      const newLoginOK = loginOK.cloneNode(true);
      loginOK.parentNode?.replaceChild(newLoginOK, loginOK);
      
      // Add click listener
      newLoginOK.addEventListener("click", () => {
        console.log("Login button clicked!");
        console.log("Username:", loginUsername?.value);
        console.log("Password:", loginPassword?.value);
        
        if (!loginUsername?.value) {
          const messageDiv = document.getElementById("gpLogInMessage");
          if (messageDiv) {
            messageDiv.innerText = "Username is required.";
            messageDiv.classList.remove("gp-hidden");
          }
          return;
        }
        
        if (!loginPassword?.value) {
          const messageDiv = document.getElementById("gpLogInMessage");
          if (messageDiv) {
            messageDiv.innerText = "Password is required.";
            messageDiv.classList.remove("gp-hidden");
          }
          return;
        }
        
        // Call your login function
        authorizeEmail(loginUsername.value, loginPassword.value);
      });
      
      console.log("Click listener attached");
    }
    
    // Remove gp-hidden class
    if (loginBox) {
      loginBox.classList.remove("gp-hidden");
      console.log("Removed gp-hidden class");
    }
    
    // Call original checkAuthorizations
    checkAuthorizations();
  });
});
</script>

<style>
.gp-login-box {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 300px;
  padding: 20px;
  background: #fff;
  border-radius: 8px;
  border: 1px solid rgba(0, 0, 0, 0.1);
  box-shadow: 0 0 1px #000000bf;
}

.gp-login-header {
  font-size: 1.3em;
  font-weight: bold;
  text-align: center;
  line-height: 2em;
}

.gp-login-slogan {
  margin: 10px 0 20px 0;
  text-align: center;
}

.gp-login-form {
  margin-top: 20px;
}

.gp-login-input {
  margin-bottom: 10px;
  padding: 8px 10px;
  width: 100%;
  font-size: 1.1em;
  border-radius: 3px;
  border: 1px solid rgba(0, 0, 0, 0.3);
  outline: none;
}

.gp-login-message {
  padding: 8px;
  font-size: 0.7em;
  background-color: rgba(255, 0, 0, 0.1);
  border: 1px solid rgba(255, 0, 0, 0.3);
  border-radius: 3px;
}

.gp-login-actions {
  margin-top: 20px;
}

.gp-login-action {
  padding: 10px;
  text-align: center;
  border-radius: 6px;
  border: 1px solid rgba(0, 0, 0, 0.1);
  cursor: pointer;
}

.gp-login-ok {
  color: #fff;
  background-color: #3f7d58;
}

.gp-login-ok:hover {
  color: #fff;
  background-color: #3f7d58dd;
}
</style>
