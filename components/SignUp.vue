<template>
  <client-only>
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
  </client-only>
</template>

<script setup lang="ts">
// Expose element IDs for the page to access
defineExpose({
  elementIds: {
    box: "gpSignUpBox",
    fullName: "gpSignUpFullName", 
    email: "gpSignUpEmail",
    password: "gpSignUpPassword",
    message: "gpSignUpMessage",
    ok: "gpSignUpOK"
  }
});
</script>