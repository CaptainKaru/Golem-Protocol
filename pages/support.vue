<script lang="ts"></script>
<template>
  <client-only>
    <NavBar :navAdminMode="'false'" />
    <div id="gpMain" class="gp-main">
      <div class="support-container">
        <h1 class="support-title">Support Page</h1>
        <h2 class="support-subtitle">Account Deletion</h2>
        <p class="support-effective-date">Effective Date: April 16, 2026</p>
        <h3 class="support-section-heading">Data Retention and Deletion</h3>
        <p class="support-body">
          You can request the deletion of your account and all associated data
          at any time. When you delete your account, all your personal data and
          inputted information will be permanently removed from our systems.
          Please contact us at
          <a class="support-link" href="mailto:codename.support@gmail.com"
            >golem.protocol.support@gmail.com</a
          >.
        </p>
      </div>
    </div>
    <Cookies />
    <Copyright />
  </client-only>
</template>

<script setup lang="ts">
import { useSeoMeta, useHead } from "@vueuse/head";
const title = "Project Golem | Home";
const description =
  "Golem Protocol is a responsive artificial intelligence system that adapts to your unique needs, learning from your behaviors and routines to provide seamless assistance across every aspect of your life.";
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
    {
      rel: "stylesheet",
      href: "https://fonts.googleapis.com/css2?family=Bitcount:wght@100..900&family=Roboto:ital,wght@0,100..900;1,100..900&display=swap",
    },
  ],
});
</script>

<style scoped></style>
<style>
.support-container {
  max-width: 760px;
  margin: 80px auto 60px;
  padding: 40px;
  background-color: #ffffff;
  border-radius: 10px;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.08);
  border: 1px solid rgba(0, 0, 0, 0.07);
}

.support-title {
  font-family: "Bitcount", "Roboto", Arial, sans-serif;
  font-size: 1.8em;
  color: #27374d;
  margin-bottom: 8px;
}

.support-subtitle {
  font-family: "Roboto", Arial, sans-serif;
  font-size: 1.1em;
  color: #30364f;
  margin-bottom: 6px;
  font-weight: 600;
}

.support-effective-date {
  font-family: "Roboto", Arial, sans-serif;
  font-size: 0.85em;
  color: #888;
  margin-bottom: 28px;
}

.support-section-heading {
  font-family: "Roboto", Arial, sans-serif;
  font-size: 1em;
  font-weight: 700;
  color: #30364f;
  margin-bottom: 10px;
  padding-bottom: 6px;
  border-bottom: 1px solid rgba(0, 0, 0, 0.08);
}

.support-body {
  font-family: "Roboto", Arial, sans-serif;
  font-size: 0.95em;
  color: #444;
  line-height: 1.75;
}

.support-link {
  color: #3f7d58;
  text-decoration: none;
  font-weight: 500;
}

.support-link:hover {
  text-decoration: underline;
}
</style>
