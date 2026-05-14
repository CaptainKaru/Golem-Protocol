<template>
  <client-only>
    <NavBar :navAdminMode="navAdminMode" />
    <div id="gpMain" class="gp-main">
      <!-- Inline the SignUp template here -->
      <div id="gpSignUpBox" class="gp-web-box gp-hidden">
        <div class="gp-web-header">Sign Up</div>
        <div class="gp-web-slogan">Make the world cleaner.</div>
        <div id="gpSignUpForm" class="gp-web-form">
          <input
            id="gpSignUpFullName"
            name="gpSignUpFullName"
            type="text"
            class="gp-web-input"
            placeholder="Full name"
            required
          />
          <input
            id="gpSignUpEmail"
            name="gpSignUpEmail"
            type="text"
            class="gp-web-input"
            placeholder="Email"
            required
          />
          <input
            id="gpSignUpPassword"
            name="gpSignUpPassword"
            type="password"
            class="gp-web-input"
            placeholder="Password"
            required
          />
        </div>
        <div id="gpSignUpMessage" class="gp-web-message gp-hidden">
          Test message...
        </div>
        <div id="gpSignUpActions" class="gp-web-actions">
          <div id="gpSignUpOK" class="gp-web-action gp-web-ok">Sign Up</div>
        </div>
      </div>
    </div>
    <Cookies />
    <Copyright />
  </client-only>
</template>

<script setup lang="ts">
import { useSeoMeta, useHead } from "@vueuse/head";
const title = "Golem Protocol | Sign Up";
const description = "Sign up for Golem Protocol";
useSeoMeta({
  title: () => title,
  description: () => description,
  charset: "utf-8",
  viewport: "width=device-width, initial-scale=1.0",
});
useHead({
  link: [
    {rel: 'icon', type: 'image/png', href: '/logo.png'},
    {rel: 'stylesheet', href: '/reset.css'},
    {rel: 'stylesheet', href: '/custom.css'} ,
    {rel: 'preconnect', href: 'https://fonts.googleapis.com'},
    {rel: 'preconnect', href: 'https://fonts.gstatic.com', crossorigin: ''},
    {rel: 'stylesheet', href: 'https://fonts.googleapis.com/css2?family=Bitcount:wght@100..900&family=Roboto:ital,wght@0,100..900;1,100..900&display=swap'}
  ],
});
const globalDelay = 500;
const cookieOptions = {
  sameSite: "none" as const,
  secure: true,
  maxAge: 60 * 60 * 24,
};
const allowCookies = useCookie<boolean>("allowCookies", cookieOptions);
allowCookies.value = allowCookies.value ?? false;
const accessToken = useCookie<string>("accessToken", cookieOptions);
accessToken.value = accessToken.value ?? "";
const userLevel = useCookie<number>("userLevel", cookieOptions);
userLevel.value = userLevel.value ?? -1;
let lastSignUpClicked = 0;
const router = useRouter();
const navAdminMode = computed(() =>
  userLevel.value >= 2 ? "gp-nav-admin" : "",
);
const gpServer = "http://localhost:5000";
type AuthResponse = {
  success: number;
  message: string;
};
function getByID<T extends HTMLElement>(id: string) {
  return document.getElementById(id) as T | null;
}
function checkAuthorizations() {
  if (accessToken.value) {
    if (userLevel.value <= 1) {
    } else if (userLevel.value >= 2) {
      router.push("/admin");
    }
  }
  const signupBox = getByID<HTMLDivElement>("gpSignUpBox");
  const signupFullName = getByID<HTMLInputElement>("gpSignUpFullName");
  const signupEmail = getByID<HTMLInputElement>("gpSignUpEmail");
  const signupPassword = getByID<HTMLInputElement>("gpSignUpPassword");
  const signupMessage = getByID<HTMLDivElement>("gpSignUpMessage");
  const signupOK = getByID<HTMLDivElement>("gpSignUpOK");
  if (
    !signupBox ||
    !signupFullName ||
    !signupEmail ||
    !signupPassword ||
    !signupMessage ||
    !signupOK
  )
    return;
  signupBox.classList.remove("gp-hidden");
  signupOK.addEventListener("click", () => {
    if (signupOK.dataset.busy == "1") return;
    const tempFullName = signupFullName.value;
    const tempEmail = signupEmail.value;
    const tempPassword = signupPassword.value;
    if (!tempFullName) {
      signupMessage.innerText = "Full name is required";
      signupMessage.classList.remove("gp-hidden");
      return;
    }
    if (!tempEmail) {
      signupMessage.innerText = "Fix email address format.";
      signupMessage.classList.remove("gp-hidden");
      return;
    }
    if (!tempPassword) {
      signupMessage.innerText = "Password must be 8–16 characters; contains at least 1 uppercase, lowercase, digit, and symbol.";
      signupMessage.classList.remove("gp-hidden");
      return;
    }
    createNewUser(tempFullName, tempEmail, tempPassword);
  });
  signupFullName.addEventListener("keyup", (e) => {
    if (e.key === "Enter" && signupFullName.value) {
      signupEmail.focus();
    }
  });
  signupEmail.addEventListener("keyup", (e) => {
    if (e.key === "Enter" && signupEmail.value) {
      signupPassword.focus();
    }
  });
  signupPassword.addEventListener("keyup", (e) => {
    if (e.key === "Enter") signupOK.click();
  });
  loadModal();
}
async function createNewUser(
  tempFullName: string,
  tempEmail: string,
  tempPassword: string,
) {
  if (lastSignUpClicked >= Date.now() - globalDelay) return;
  lastSignUpClicked = Date.now();
  const signupFullName = getByID<HTMLInputElement>("gpSignUpFullName");
  const signupEmail = getByID<HTMLInputElement>("gpSignUpEmail");
  const signupPassword = getByID<HTMLInputElement>("gpSignUpPassword");
  const signupMessage = getByID<HTMLDivElement>("gpSignUpMessage");
  const signupOK = getByID<HTMLDivElement>("gpSignUpOK");
  if (
    !signupFullName ||
    !signupEmail ||
    !signupPassword ||
    !signupOK ||
    !signupMessage
  )
    return;
  let isSuccessful = false;
  signupMessage.innerText = "";
  signupMessage.classList.add("gp-hidden");
  [signupFullName, signupEmail, signupPassword].forEach(
    (el) => (el.disabled = true),
  );
  signupOK.dataset.busy = "1";
  try {
    const response = (await $fetch(`${gpServer}/signup`, {
      headers: { "Content-Type": "application/json" },
      method: "POST",
      body: {
        fullName: tempFullName,
        email: tempEmail,
        password: tempPassword,
      },
    })) as AuthResponse;
    isSuccessful = Boolean(response.success === 1);
    if (response.message) {
      signupMessage.innerText = response.message;
      signupMessage.classList.remove("gp-hidden");
    }
  } catch (e: any) {
    signupMessage.innerText = `Error encountered: ${e}`;
    signupMessage.classList.remove("gp-hidden");
  } finally {
    signupOK.dataset.busy = "0";
  }
  [signupFullName, signupEmail, signupPassword].forEach(
    (el) => (el.disabled = false),
  );
  signupOK.dataset.busy = "0";
  if (isSuccessful) {
    [signupFullName, signupEmail, signupPassword, signupOK].forEach((el) =>
      el.classList.add("gp-hidden"),
    );
    signupMessage.innerText = "Sign in after email confirmation is received.";
    signupMessage.classList.remove("gp-hidden");
  }
}
function loadModal() {
  const cookieX = getByID<HTMLDivElement>("gpCookieX");
  const cookieOK = getByID<HTMLDivElement>("gpCookieOK");
  if (!cookieX || !cookieOK) return;
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
  if (!cookieBox || !cookieModal) return;
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
  nextTick(checkAuthorizations);
});
</script>