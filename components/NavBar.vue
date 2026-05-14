<template>
  <client-only>
    <header :class="['gp-navbar', navAdminMode]">
      <nav class="gp-nav-left">
        <a href="/" class="gp-nav-home">
          <img src="/logo.png" width="20" height="20" class="gp-nav-logo">
          <span>Golem Protocol</span>
        </a>
      </nav>

      <!-- Guest navigation (shown when not logged in, userLevel === -1) -->
      <nav id="gpNavGuest" class="gp-nav-right" v-if="userLevel === -1">
        <ul>
          <li><a href="/signup" class="gp-nav-link">Sign up</a></li>
          <li><a href="/signin" class="gp-nav-link">Sign in</a></li>
        </ul>
      </nav>

      <!-- Basic user navigation (shown when logged in as regular user, userLevel === 1) -->
      <nav id="gpNavBasic" class="gp-nav-right" v-else-if="userLevel === 1">
        <ul>
          <li><a href="#" class="gp-nav-link">3R Guide</a></li>
          <li><a href="#" class="gp-nav-link">Leaderboard</a></li>
          <li><a href="#" class="gp-nav-link">Contribute</a></li>
          <li><span class="gp-nav-link" @click="logout">Logout</span></li>
        </ul>
      </nav>

      <!-- Admin navigation (shown when logged in as admin, userLevel >= 2) -->
      <nav id="gpNavAdmin" class="gp-nav-right" v-else-if="userLevel >= 2">
        <ul>
          <li><a href="#" class="gp-nav-link">Settings</a></li>
          <li><a href="#" class="gp-nav-link">Reports</a></li>
          <li><span class="gp-nav-link" @click="logout">Logout</span></li>
        </ul>
      </nav>
    </header>
  </client-only>
</template>

<script setup lang="ts">
const props = defineProps<{ navAdminMode: string }>();

// Get user state from cookies
const userLevel = useCookie<number>("userLevel");
const accessToken = useCookie<string>("accessToken");
const emailAddress = useCookie<string>("emailAddress");
const fullName = useCookie<string>("fullName");

const router = useRouter();

function logout() {
  // Clear all auth cookies
  accessToken.value = "";
  userLevel.value = -1;
  emailAddress.value = "";
  fullName.value = "";
  
  // Redirect to home page
  router.push("/");
}
</script>