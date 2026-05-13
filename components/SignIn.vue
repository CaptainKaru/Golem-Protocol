<template>
  <client-only>
    <div id="gpSignInBox" class="gp-web-box gp-hidden">
      <div class="gp-web-header">Sign In</div>
      <div class="gp-web-slogan">Make the world cleaner.</div>
      <div id="gpSignInForm" class="gp-web-form">
        <input
          id="gpSignInEmail"
          name="gpSignInEmail"
          type="text"
          class="gp-web-input"
          placeholder="Email"
          required
        />
        <input
          id="gpSignInPassword"
          name="gpSignInPassword"
          type="password"
          class="gp-web-input"
          placeholder="Password"
          required
        />
      </div>
      <div id="gpSignInMessage" class="gp-web-message gp-hidden">
        Test message...
      </div>
      <div id="gpSignInActions" class="gp-web-actions">
        <div id="gpSignInOK" class="gp-web-action gp-web-ok">Sign In</div>
      </div>
    </div>
  </client-only>
</template>