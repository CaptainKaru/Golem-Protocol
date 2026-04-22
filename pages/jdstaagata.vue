<script lang="ts"></script>
<template>
  <client-only>
    <NavBar :navAdminMode="'false'" />
    <div id="gpMain" class="gp-main">
      <div class="personal-container">
        <img src="/jerome.png" alt="Jerome Daniel Sta. Agata" class="personal-img" />

        <div class="personal-header-anim">
          <h1 class="personal-name">Jerome Daniel <p>Sta. Agata</p></h1>
          <p class="personal-handle">staagatadaniel@gmail.com</p>
          <p class="personal-bio">
            I build things for the web — mostly frontend, sometimes backend, always curious.
            Computer Science student figuring out one stack at a time.
          </p>
        </div>

        <div class="personal-divider"></div>

        <section class="personal-section" style="--delay: 0.1s">
          <h2 class="personal-section-title">Work Experience</h2>

          <div class="personal-entry">
            <div class="personal-entry-header">
              <span class="personal-role">App Dev Team Member | Dagan Choy</span>
              <span class="personal-period">2025</span>
            </div>
            <p class="personal-entry-desc">
              Collaborated on a live currency exchange rate dashboard built with Nuxt.js and Flask,
              featuring cookie-based authentication and role-based routing.
            </p>
          </div>
        </section>

        <div class="personal-divider" style="--delay: 0.2s"></div>

        <section class="personal-section" style="--delay: 0.3s">
          <h2 class="personal-section-title">Projects</h2>

          <div class="personal-entry">
            <div class="personal-entry-header">
              <span class="personal-role">VizForge</span>
            </div>
            <p class="personal-entry-desc">
              AI-powered DSA algorithm visualizer. Takes a LeetCode-style problem and renders
              step-by-step animated visualizations using Groq and Framer Motion.
            </p>
          </div>

          <div class="personal-entry">
            <div class="personal-entry-header">
              <span class="personal-role">Code Scanner</span>
            </div>
            <p class="personal-entry-desc">
              Static code analyzer that scans for OWASP Top 10 vulnerabilities with an
              AI-powered analysis panel and PDF/JSON export.
            </p>
          </div>

          <div class="personal-entry">
            <div class="personal-entry-header">
              <span class="personal-role">GitHub Repo Analyzer</span>
            </div>
            <p class="personal-entry-desc">
              Analyzes GitHub repositories for stats, contributors, stack detection,
              and README summaries using the Gemini API.
            </p>
          </div>

          <div class="personal-entry">
            <div class="personal-entry-header">
              <span class="personal-role">Vault</span>
            </div>
            <p class="personal-entry-desc">
              A fullstack personal finance tracking system with complete Frontend and Backend with Database and realtime dashboard.
            </p>
          </div>
        </section>

        <div class="personal-divider" style="--delay: 0.4s"></div>

        <section class="personal-section" style="--delay: 0.5s">
          <h2 class="personal-section-title">Skills</h2>
          <ul class="personal-skills">
            <li>Next.js / Nuxt.js</li>
            <li>TypeScript</li>
            <li>Tailwind CSS</li>
            <li>Node.js / Express</li>
            <li>PostgreSQL</li>
            <li>Git / GitHub</li>
          </ul>
        </section>
      </div>
    </div>
    <Cookies />
    <Copyright />
  </client-only>
</template>

<script setup lang="ts">
import { useSeoMeta, useHead } from "@vueuse/head";
const title = "Jerome Daniel Sta. Agata";
const description = "The personal page of Jerome Daniel Sta. Agata.";
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

<style scoped>
/* Base Keyframes */
@keyframes fadeUp {
  0% {
    opacity: 0;
    transform: translateY(20px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes pulseGlow {
  0% {
    box-shadow: 0 0 0 0 rgba(39, 55, 77, 0.4);
  }
  70% {
    box-shadow: 0 0 0 10px rgba(39, 55, 77, 0);
  }
  100% {
    box-shadow: 0 0 0 0 rgba(39, 55, 77, 0);
  }
}

/* Container Styling */
.personal-container {
  max-width: 680px;
  margin: 80px auto 60px;
  padding: 56px 48px;
  background: linear-gradient(145deg, #ffffff, #fcfcfc);
  border-radius: 16px;
  box-shadow: 0 10px 40px rgba(0, 0, 0, 0.06), 0 2px 10px rgba(0, 0, 0, 0.04);
  border: 1px solid rgba(0, 0, 0, 0.05);
  position: relative;
  overflow: hidden;
  animation: fadeUp 0.8s cubic-bezier(0.16, 1, 0.3, 1) forwards;
}

.personal-container::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 4px;
  background: linear-gradient(90deg, #27374d, #3f7d58);
}

/* Avatar Styling */
.personal-avatar-placeholder {
  width: 88px;
  height: 88px;
  border-radius: 50%;
  background: linear-gradient(135deg, #27374d, #3f7d58);
  color: #fff;
  font-family: "Bitcount", sans-serif;
  font-size: 1.6em;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 24px;
  box-shadow: 0 4px 15px rgba(39, 55, 77, 0.2);
  transition: transform 0.4s cubic-bezier(0.34, 1.56, 0.64, 1);
  animation: pulseGlow 3s infinite;
}

.personal-avatar-placeholder:hover {
  transform: scale(1.08) rotate(-5deg);
}

.personal-img {
  width: 88px;
  height: 88px;
  border-radius: 50%;
  object-fit: cover;
  object-position: center; /* Ensures the image subject is centered */
  background-color: #ffffff; /* Adds a clean background just in case your image has transparency */
  margin-bottom: 24px;
  border: 3px solid #fff;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
  transition: transform 0.4s cubic-bezier(0.34, 1.56, 0.64, 1);
  animation: pulseGlow 3s infinite; /* Restored the glowing pulse animation! */
}

.personal-img:hover {
  transform: scale(1.08) rotate(-5deg); /* Brought back the playful tilt from the original placeholder */
}

/* Header Typography */
.personal-header-anim {
  opacity: 0;
  animation: fadeUp 0.6s cubic-bezier(0.16, 1, 0.3, 1) forwards;
  animation-delay: 0.1s;
}

.personal-name {
  font-family: "Bitcount", "Roboto", Arial, sans-serif;
  font-size: 2.2em;
  color: #1a2332;
  margin-bottom: 4px;
  letter-spacing: -0.02em;
}

.personal-handle {
  font-family: "Roboto", Arial, sans-serif;
  font-size: 0.9em;
  color: #3f7d58;
  margin-bottom: 18px;
  font-weight: 500;
  display: inline-block;
  position: relative;
}

.personal-handle::after {
  content: "";
  position: absolute;
  width: 100%;
  transform: scaleX(0);
  height: 1px;
  bottom: 0;
  left: 0;
  background-color: #3f7d58;
  transform-origin: bottom right;
  transition: transform 0.25s ease-out;
}

.personal-handle:hover::after {
  transform: scaleX(1);
  transform-origin: bottom left;
}

.personal-bio {
  font-family: "Roboto", Arial, sans-serif;
  font-size: 1em;
  color: #555;
  line-height: 1.8;
  max-width: 95%;
}

/* Section Dividers */
.personal-divider {
  border: none;
  height: 1px;
  background: linear-gradient(90deg, rgba(0,0,0,0.02) 0%, rgba(0,0,0,0.08) 50%, rgba(0,0,0,0.02) 100%);
  margin: 36px 0;
  opacity: 0;
  animation: fadeUp 0.6s cubic-bezier(0.16, 1, 0.3, 1) forwards;
  animation-delay: var(--delay);
}

/* Section Styling */
.personal-section {
  opacity: 0;
  animation: fadeUp 0.6s cubic-bezier(0.16, 1, 0.3, 1) forwards;
  animation-delay: var(--delay);
}

.personal-section-title {
  font-family: "Roboto", Arial, sans-serif;
  font-size: 0.85em;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.15em;
  color: #8892b0;
  margin-bottom: 20px;
  display: flex;
  align-items: center;
  gap: 12px;
}

.personal-section-title::after {
  content: "";
  flex: 1;
  height: 1px;
  background-color: rgba(0, 0, 0, 0.04);
}

/* Entry Styling */
.personal-entry {
  margin-bottom: 24px;
  padding: 16px 20px;
  border-radius: 10px;
  background-color: transparent;
  border: 1px solid transparent;
  transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
  margin-left: -20px;
  margin-right: -20px;
}

.personal-entry:hover {
  background-color: #f8fafc;
  border: 1px solid rgba(0, 0, 0, 0.03);
  transform: translateY(-2px);
  box-shadow: 0 6px 16px rgba(0, 0, 0, 0.04);
}

.personal-entry-header {
  display: flex;
  justify-content: space-between;
  align-items: baseline;
  flex-wrap: wrap;
  gap: 8px;
  margin-bottom: 8px;
}

.personal-role {
  font-family: "Roboto", Arial, sans-serif;
  font-size: 1.05em;
  font-weight: 600;
  color: #27374d;
  transition: color 0.2s ease;
}

.personal-entry:hover .personal-role {
  color: #3f7d58;
}

.personal-period {
  font-family: "Roboto", Arial, sans-serif;
  font-size: 0.85em;
  color: #94a3b8;
  font-weight: 500;
  background-color: #f1f5f9;
  padding: 2px 8px;
  border-radius: 12px;
}

.personal-entry-desc {
  font-family: "Roboto", Arial, sans-serif;
  font-size: 0.95em;
  color: #64748b;
  line-height: 1.75;
}

/* Skills Tags */
.personal-skills {
  list-style: none;
  padding: 0;
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
}

.personal-skills li {
  font-family: "Roboto", Arial, sans-serif;
  font-size: 0.85em;
  font-weight: 500;
  color: #475569;
  background-color: #f1f5f9;
  border: 1px solid rgba(0, 0, 0, 0.04);
  border-radius: 6px;
  padding: 6px 14px;
  transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
  cursor: default;
}

.personal-skills li:hover {
  background-color: #3f7d58;
  color: #ffffff;
  border-color: #3f7d58;
  transform: translateY(-3px);
  box-shadow: 0 4px 10px rgba(63, 125, 88, 0.25);
}
</style>