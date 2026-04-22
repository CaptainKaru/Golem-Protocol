<script lang="ts"></script>

<template>
  <client-only>
    <!-- NAV -->
    <div class="kyla-portfolio-page">
    <nav id="gpNav" class="nav">
      <a href="/" @click="forceReload" class="nav-logo">
        <div class="nav-logo">
          <span class="nav-logo-mark">✦</span>
          <span class="nav-logo-text">BLUEBIRD</span>
        </div>
      </a>
      <div class="nav-links">
        <a href="#home" class="nav-link">Home</a>
        <a href="#about" class="nav-link">About</a>
        <a href="#work" class="nav-link">Work</a>
        <a href="#contact" class="nav-link">Contact</a>
      </div>
      <div class="nav-badge">OPEN TO WORK</div>
    </nav>

    <!-- HERO -->
    <section id="home" class="hero">
      <div class="hero-grid-overlay"></div>
      <div class="hero-tag top-left">
        <span class="tag tag-green">PORTFOLIO ✦</span>
        <span class="tag tag-outline">2026</span>
      </div>
      <div class="hero-content">
        <div class="hero-title-block">
          <p class="hero-eyebrow">Creative Design &amp; Coding</p>
          <h1 class="hero-title">
            <span class="title-outline">KYLA GAYLE DELIMA</span><br>
            <span class="title-fill">PORTFOLIO.</span>
          </h1>
        </div>
        <div class="hero-right">
          <div class="hero-photo-frame">
            <img src="/kai1.png" alt="Kyla Gayle Delima" class="hero-photo" />
            <div class="hero-photo-deco">✦</div>
          </div>
          <div class="hero-blurb">
            <div class="blurb-badge">AKA bluebird / bluebirbb</div>
          </div>
        </div>
      </div>
      <div class="hero-bottom">
        <div class="hero-name-tag">▶ KYLA GAYLE</div>
        <div class="hero-marquee-wrap">
          <div class="hero-marquee">
            <span>CREATIVE DESIGN ✦ ILLUSTRATION ✦ FRONT-END DEV ✦ GRAPHIC DESIGN ✦ WEB DEV ✦ CREATIVE DESIGN ✦ ILLUSTRATION ✦ FRONT-END DEV ✦ GRAPHIC DESIGN ✦&nbsp;</span>
          </div>
        </div>
      </div>
    </section>

    <!-- ABOUT -->
    <section id="about" class="about section">
      <div class="section-label">About ——————</div>
      <div class="about-grid">
        <div class="about-photo-col">
          <div class="about-photo-frame">
            <img src="/kai3.png" alt="kai" class="about-photo" />
          </div>
          <div class="about-contact-card">
            <p class="contact-card-title">Let's Work Together :</p>
            <a href="kgdelima.work@gmail.com" class="contact-item">✉ kgdelima.work@gmail.com</a>
            <a href="tel:+639913142424" class="contact-item">✆ 0991 314 2424</a>
            <a href="https://instagram.com/kaii.kite" target="_blank" class="contact-item">◎ @kaii.kite</a>
            <a href="https://linkedin.com/in/dkylagayle" target="_blank" class="contact-item">in linkedin.com/in/dkylagayle</a>
          </div>
        </div>

        <div class="about-text-col">
          <h2 class="about-hello">HEYAAA ⸜(｡˃ ᵕ ˂ )⸝♡</h2>
          <p class="about-bio">
            I'm <strong>Kyla Gayle Delima</strong>, a self-taught graphic designer &amp; a computer science student. I love creating designs that have pops of color, and geometry. From posters to brochures to illustrations and digital experiences, I enjoy exploring new techniques and incorporating colors into my art.
          </p>
          <div class="about-details-grid">
            <div class="about-edu">
              <p class="detail-label">Education</p>
              <p class="detail-year">2024-Present</p>
              <p class="detail-main">Bachelor of Science in Computer Science</p>
              <p class="detail-sub">Visayas State University</p>
            </div>
            <div class="about-skills">
              <p class="detail-label">Software & Skills</p>
              <div class="skill-pills">
                <span class="pill pill-blue">Figma</span>
                <span class="pill pill-green">Photoshop</span>
                <span class="pill pill-outline">HTML</span>
                <span class="pill pill-blue">C/C++</span>
                <span class="pill pill-green">Illustrator</span>
                <span class="pill pill-outline">CSS</span>
                
                <span class="pill pill-blue">Java</span>
                <span class="pill pill-green">Canva</span>
              </div>
            </div>
          </div>

          <div class="about-experience">
            <p class="detail-label">Working Experience</p>
            <div class="exp-grid">
              <div class="exp-item">
                <p class="exp-role">Data Analyst</p>
                <p class="exp-company">Warwick</p>
                <p class="exp-date">Dec 2021 – 2022</p>
              </div>
              <div class="exp-item">
                <p class="exp-role">Sales Rep/Social Media Manager</p>
                <p class="exp-company">KYUBI</p>
                <p class="exp-date">March 2026 – Present</p>
              </div>
              <div class="exp-item">
                <p class="exp-role">Freelance Designer</p>
                <p class="exp-company">Self-employed</p>
                <p class="exp-date">2019 – Present</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- WORK / PORTFOLIO GRID -->
    <section id="work" class="work section">
      <div class="section-label">Selected Work ——————</div>
      <div class="work-header">
        <span class="tag tag-green">PROJECTS ✦</span>
        <h2 class="work-title">RECENT WORK.</h2>
      </div>
      <div class="work-grid">
        <div class="work-card work-card-wide">
          <div class="work-card-img-wrap">
            <img src="/newsletter.png" alt="Project 1" class="work-card-img" />
          </div>
          <div class="work-card-info">
            <span class="work-card-cat">School Paper Layout</span>
            <h3 class="work-card-title">The End of an Era</h3>
            <p class="work-card-desc">Layout for The Science Net 2018</p>
          </div>
        </div>
        <div class="work-card">
          <div class="work-card-img-wrap">
            <img src="/ryo.gif" alt="Project 2" class="work-card-img" />
          </div>
          <div class="work-card-info">
            <span class="work-card-cat">Pixel Art</span>
            <h3 class="work-card-title">No money? Eat Grass.</h3>
            <p class="work-card-desc">A pixel art of Yamada Ryo from Bocchi The Rock eating grass because she ran out of money lol </p>
          </div>
        </div>
        <div class="work-card">
          <div class="work-card-img-wrap">
            <img src="/taru.jpg" alt="Project 3" class="work-card-img" />
          </div>
          <div class="work-card-info">
            <span class="work-card-cat">Illustration</span>
            <h3 class="work-card-title">The Boy and his Cats</h3>
            <p class="work-card-desc">Art I made for a friend on his birthday</p>
          </div>
        </div>
      </div>
    </section>

    <!-- CONTACT -->
    <section id="contact" class="contact-section section">
      <div class="section-label">Get In Touch ——————</div>
      <div class="contact-inner">
        <div class="contact-sticker">touch it +</div>
        <h2 class="contact-heading">LET'S CREATE<br><span class="contact-heading-outline">SOMETHING.</span></h2>
        <p class="contact-sub">Have a project in mind? Let's talk.</p>
        <a href="kgdelima.work@gmail.com" class="contact-cta">kgdelima.work@gmail.com ✦</a>
        <div class="contact-socials">
          <a href="https://instagram.com/kaii.kite" target="_blank" class="social-link">Instagram</a>
          <a href="https://linkedin.com/in/dkylagayle" target="_blank" class="social-link">LinkedIn</a>
          <a href="https://facebook.com/depayb/" target="_blank" class="social-link">Facebook</a>
          <a href="https://github.com/bluebirbb" target="_blank" class="social-link">GitHub</a>
        </div>
      </div>
    </section>

    <!-- FOOTER -->
    <footer class="footer">
      <div class="footer-grid">
        <div class="footer-brand">
          <span class="footer-logo-mark">✦</span>
          <span class="footer-logo-text">BLUEBIRD</span>
          <p class="footer-tagline">Creative Design &amp; Coding · 2025</p>
        </div>
        <div class="footer-nav">
          <a href="#home" class="footer-link">Home</a>
          <a href="#about" class="footer-link">About</a>
          <a href="#work" class="footer-link">Work</a>
          <a href="#contact" class="footer-link">Contact</a>
        </div>
        <div class="footer-socials">
          <a href="https://instagram.com/kaii.kite" target="_blank" class="footer-link">Instagram</a>
          <a href="https://linkedin.com/in/dkylagayle" target="_blank" class="footer-link">LinkedIn</a>
          <a href="https://facebook.com/depayb/" target="_blank" class="footer-link">Facebook</a>
          <a href="https://github.com/bluebirbb" target="_blank" class="footer-link">GitHub</a>
        </div>
      </div>
      <div class="footer-bottom">
        <span>© 2026 BLUEBIRD. All rights reserved.</span>
        <span class="footer-made">Made with ✦ and a lot of matcha</span>
      </div>
    </footer>
    </div>
  </client-only>
</template>

<script setup lang="ts">
import { useSeoMeta, useHead } from "@vueuse/head";
import { onMounted } from "vue";

const title = "Kyla Delima — Creative Portfolio";
const description = "Creative visual designer, photographer, and developer based in the Philippines.";

useSeoMeta({
  title: () => title,
  description: () => description,
  charset: "utf-8",
  viewport: "width=device-width, initial-scale=1.0",
});

useHead({
  link: [
    { rel: "icon", type: "image/png", href: "/logo.png" },
    { rel: "preconnect", href: "https://fonts.googleapis.com" },
    { rel: "preconnect", href: "https://fonts.gstatic.com", crossorigin: "" },
    {
      rel: "stylesheet",
      href: "https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Space+Grotesk:wght@300;400;500;600;700&family=Caveat:wght@400;700&display=swap",
    },
  ],
});

const forceReload = (e: MouseEvent) => {
  window.location.href = '/';
};

onMounted(() => {
  document.querySelectorAll('a[href^="#"]').forEach((anchor) => {
    anchor.addEventListener("click", (e) => {
      e.preventDefault();
      const target = document.querySelector((anchor as HTMLAnchorElement).getAttribute("href")!);
      if (target) target.scrollIntoView({ behavior: "smooth" });
    });
  });

  const observer = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add("visible");
        }
      });
    },
    { threshold: 0.1, rootMargin: "0px 0px -50px 0px" }
  );

  const elements = document.querySelectorAll(".section, .work-card, .toc-card");
  
  // Fallback: force visible after 800ms in case observer doesn't fire
  setTimeout(() => {
    elements.forEach((el) => el.classList.add("visible"));
  }, 800);

  elements.forEach((el) => observer.observe(el));
});
</script>

<style scoped>
.kyla-portfolio-page {
  --blue: #0fa3e2;
  --blue-dark: #0a7ab3;
  --green: #9cff57;
  --black: #111111;
  --white: #f5f5f0;
  --gray: #888;
  --border: rgba(0,0,0,0.12);
  --font-display: 'Bebas Neue', sans-serif;
  --font-body: 'Space Grotesk', sans-serif;
  --font-script: 'Caveat', cursive;
}

.kyla-portfolio-page .nav {
  position: fixed;
  top: 0; left: 0; right: 0;
  z-index: 100;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 18px 5%;
  background: var(--white);
  border-bottom: 1.5px solid var(--border);
}

.kyla-portfolio-page .nav-logo { display: flex; align-items: center; gap: 8px; }

:root {
  --blue: #0fa3e2;
  --blue-dark: #0a7ab3;
  --green: #9cff57;
  --black: #111111;
  --white: #f5f5f0;
  --gray: #888;
  --border: rgba(0,0,0,0.12);
  --font-display: 'Bebas Neue', sans-serif;
  --font-body: 'Space Grotesk', sans-serif;
  --font-script: 'Caveat', cursive;
}

*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
html { scroll-behavior: smooth; }
body {
  background: var(--white);
  color: var(--black);
  font-family: var(--font-body);
  overflow-x: hidden;
}
img { width: 100%; height: 100%; object-fit: cover; display: block; }
a { text-decoration: none; color: inherit; }

.section {
  padding: 80px 5%;
  opacity: 1;
  transform: none;
}
.section.visible { opacity: 1; transform: none; }

.section-label {
  font-family: var(--font-body);
  font-size: 0.72rem;
  font-weight: 600;
  letter-spacing: 0.18em;
  text-transform: uppercase;
  color: var(--gray);
  margin-bottom: 32px;
}

.tag {
  display: inline-block;
  padding: 4px 12px;
  border-radius: 999px;
  font-size: 0.72rem;
  font-weight: 700;
  letter-spacing: 0.12em;
  text-transform: uppercase;
}
.tag-green { background: var(--green); color: var(--black); }
.tag-outline { border: 1.5px solid var(--black); color: var(--black); }
.tag-blue { background: var(--blue); color: #fff; }

.hero-grid-overlay {
  position: absolute;
  inset: 0;
  background-image:
    linear-gradient(rgba(0,0,0,0.06) 1px, transparent 1px),
    linear-gradient(90deg, rgba(0,0,0,0.06) 1px, transparent 1px);
  background-size: 32px 32px;
  pointer-events: none;
  z-index: 0;
}

.nav {
  position: fixed;
  top: 0; left: 0; right: 0;
  z-index: 100;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 18px 5%;
  background: var(--white);
  border-bottom: 1.5px solid var(--border);
}
.nav-logo { display: flex; align-items: center; gap: 8px; }
.nav-logo-mark { font-size: 1.1rem; color: var(--blue); }
.nav-logo-text {
  font-family: var(--font-display);
  font-size: 1.4rem;
  letter-spacing: 0.08em;
  color: var(--black);
}
.nav-links { display: flex; gap: 32px; }
.nav-link {
  font-size: 0.82rem;
  font-weight: 600;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: var(--black);
  transition: color 0.2s;
}
.nav-link:hover { color: var(--blue); }
.nav-badge {
  background: var(--green);
  color: var(--black);
  font-size: 0.65rem;
  font-weight: 800;
  letter-spacing: 0.14em;
  text-transform: uppercase;
  padding: 5px 12px;
  border-radius: 999px;
}

.hero {
  position: relative;
  min-height: 100vh;
  padding: 120px 5% 60px;
  display: flex;
  flex-direction: column;
  overflow: hidden;
  background: var(--white);
}
.hero-tag.top-left {
  position: relative;
  z-index: 1;
  display: flex;
  gap: 8px;
  margin-bottom: 20px;
}
.hero-content {
  position: relative;
  z-index: 1;
  display: grid;
  grid-template-columns: 1fr auto;
  gap: 40px;
  align-items: center;
  flex: 1;
}
.hero-eyebrow {
  font-family: var(--font-script);
  font-size: 1.2rem;
  color: var(--blue);
  margin-bottom: 4px;
}
.hero-title {
  font-family: var(--font-display);
  font-size: clamp(5rem, 13vw, 10rem);
  line-height: 0.92;
  letter-spacing: 0.01em;
}
.title-outline {
  -webkit-text-stroke: 2px var(--black);
  color: transparent;
}
.title-fill { color: var(--black); }

.hero-right {
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  gap: 16px;
}
.hero-photo-frame {
  position: relative;
  width: 260px;
  height: 320px;
  border-radius: 12px;
  overflow: hidden;
  border: 3px solid var(--black);
  background: #ccc;
}
.hero-photo-frame .hero-photo { width: 100%; height: 100%; object-fit: cover; }
.hero-photo-deco {
  position: absolute;
  bottom: 12px; right: 14px;
  font-size: 1.5rem;
  color: var(--green);
  font-weight: 900;
}
.hero-blurb { display: flex; justify-content: flex-end; }
.blurb-badge {
  background: var(--blue);
  color: #fff;
  padding: 10px 16px;
  border-radius: 8px;
  font-size: 0.75rem;
  font-weight: 700;
  text-align: right;
  line-height: 1.5;
  letter-spacing: 0.05em;
  text-transform: uppercase;
}

.hero-bottom {
  position: relative;
  z-index: 1;
  margin-top: 40px;
  border-top: 1.5px solid var(--border);
  padding-top: 20px;
  display: flex;
  align-items: center;
  gap: 24px;
  overflow: hidden;
}
.hero-name-tag {
  white-space: nowrap;
  font-size: 0.8rem;
  font-weight: 700;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  flex-shrink: 0;
}
.hero-marquee-wrap { overflow: hidden; flex: 1; }
.hero-marquee {
  display: flex;
  animation: marquee 18s linear infinite;
  white-space: nowrap;
}
.hero-marquee span {
  font-size: 0.75rem;
  font-weight: 600;
  letter-spacing: 0.14em;
  color: var(--gray);
  text-transform: uppercase;
}
@keyframes marquee {
  from { transform: translateX(0); }
  to { transform: translateX(-50%); }
}

.about { background: var(--white); }
.about-grid {
  display: grid;
  grid-template-columns: 300px 1fr;
  gap: 60px;
  align-items: start;
}
.about-photo-frame {
  width: 100%;
  aspect-ratio: 5/9;
  border-radius: 12px;
  overflow: hidden;
  border: 3px solid var(--black);
  background: #ccc;
  margin-bottom: 20px;
}
.about-contact-card {
  background: var(--black);
  color: var(--white);
  padding: 20px;
  border-radius: 10px;
  display: flex;
  flex-direction: column;
  gap: 8px;
}
.contact-card-title {
  font-size: 0.72rem;
  font-weight: 700;
  letter-spacing: 0.14em;
  text-transform: uppercase;
  color: var(--green);
  margin-bottom: 6px;
}
.contact-item {
  font-size: 0.8rem;
  color: rgba(255,255,255,0.8);
  transition: color 0.2s;
}
.contact-item:hover { color: var(--green); }

.about-hello {
  font-family: var(--font-display);
  font-size: 3.5rem;
  color: var(--black);
  margin-bottom: 16px;
}
.about-bio {
  font-size: 0.92rem;
  line-height: 1.75;
  color: #444;
  max-width: 560px;
  margin-bottom: 36px;
}
.about-bio strong { color: var(--black); }
.about-details-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 32px;
  margin-bottom: 36px;
}
.detail-label {
  font-size: 0.72rem;
  font-weight: 700;
  letter-spacing: 0.14em;
  text-transform: uppercase;
  color: var(--blue);
  margin-bottom: 10px;
  border-bottom: 1.5px solid var(--border);
  padding-bottom: 6px;
}
.detail-year { font-size: 0.75rem; color: var(--gray); }
.detail-main { font-size: 0.88rem; font-weight: 600; margin-top: 2px; }
.detail-sub { font-size: 0.78rem; color: var(--gray); }
.skill-pills { display: flex; flex-wrap: wrap; gap: 8px; }
.pill {
  padding: 4px 12px;
  border-radius: 999px;
  font-size: 0.73rem;
  font-weight: 600;
  letter-spacing: 0.06em;
}
.pill-blue { background: var(--blue); color: #fff; }
.pill-green { background: var(--green); color: var(--black); }
.pill-outline { border: 1.5px solid var(--black); color: var(--black); }

.exp-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 20px; }
.exp-item { border-left: 3px solid var(--green); padding-left: 12px; }
.exp-role { font-size: 0.85rem; font-weight: 700; }
.exp-company { font-size: 0.78rem; color: var(--blue); margin-top: 2px; }
.exp-date { font-size: 0.72rem; color: var(--gray); margin-top: 2px; }

.services { background: var(--black); color: var(--white); }
.services .section-label { color: rgba(255,255,255,0.4); }
.toc-heading {
  font-family: var(--font-display);
  font-size: clamp(2.5rem, 6vw, 5rem);
  letter-spacing: 0.02em;
  margin-bottom: 48px;
  -webkit-text-stroke: 1.5px rgba(255,255,255,0.5);
  color: transparent;
}
.toc-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 16px;
}
.toc-card {
  padding: 36px 24px;
  border-radius: 12px;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 16px;
  transition: transform 0.25s ease;
  cursor: default;
}
.toc-card:hover { transform: translateY(-6px); }
.toc-card-blue { background: var(--blue); color: #fff; }
.toc-card-green { background: var(--green); color: var(--black); }
.toc-card-outline { border: 2px solid rgba(255,255,255,0.2); color: var(--white); }
.toc-icon { font-size: 2rem; }
.toc-label { font-size: 0.92rem; font-weight: 600; text-align: center; line-height: 1.4; }

.work { background: var(--white); }
.work-header {
  display: flex;
  align-items: center;
  gap: 16px;
  margin-bottom: 40px;
}
.work-title {
  font-family: var(--font-display);
  font-size: clamp(2.5rem, 6vw, 4.5rem);
  letter-spacing: 0.02em;
}
.work-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 20px;
}
.work-card-wide { grid-column: span 2; }
.work-card {
  border-radius: 12px;
  overflow: hidden;
  border: 1.5px solid var(--border);
  opacity: 1;
  transform: none;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}
.work-card.visible { opacity: 1; transform: none; }
.work-card:hover { transform: translateY(-6px); box-shadow: 0 12px 40px rgba(0,0,0,0.12); }
.work-card-img-wrap {
  width: 100%;
  aspect-ratio: 16/9;
  background: #d0d0d0;
  overflow: hidden;
}
.work-card-wide .work-card-img-wrap { aspect-ratio: 21/9; }
.work-card-img { transition: transform 0.5s ease; }
.work-card:hover .work-card-img { transform: scale(1.04); }
.work-card-info { padding: 20px 24px; }
.work-card-cat {
  font-size: 0.7rem;
  font-weight: 700;
  letter-spacing: 0.14em;
  text-transform: uppercase;
  color: var(--blue);
}
.work-card-title {
  font-family: var(--font-display);
  font-size: 1.5rem;
  margin: 4px 0;
  letter-spacing: 0.03em;
}
.work-card-desc { font-size: 0.82rem; color: var(--gray); line-height: 1.6; }

.contact-section {
  background: var(--blue);
  color: #fff;
  text-align: center;
}
.contact-section .section-label { color: rgba(255,255,255,0.6); text-align: left; }
.contact-inner { max-width: 640px; margin: 0 auto; padding-top: 20px; }
.contact-sticker {
  display: inline-block;
  background: var(--green);
  color: var(--black);
  font-size: 0.75rem;
  font-weight: 800;
  letter-spacing: 0.14em;
  text-transform: uppercase;
  padding: 6px 16px;
  border-radius: 999px;
  margin-bottom: 28px;
}
.contact-heading {
  font-family: var(--font-display);
  font-size: clamp(3rem, 8vw, 6rem);
  line-height: 0.92;
  margin-bottom: 16px;
}
.contact-heading-outline {
  -webkit-text-stroke: 2px #fff;
  color: transparent;
}
.contact-sub { font-size: 1rem; opacity: 0.8; margin-bottom: 32px; }
.contact-cta {
  display: inline-block;
  background: var(--black);
  color: var(--white);
  padding: 16px 36px;
  border-radius: 8px;
  font-size: 0.9rem;
  font-weight: 700;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  transition: background 0.2s, transform 0.2s;
  margin-bottom: 40px;
}
.contact-cta:hover { background: var(--green); color: var(--black); transform: translateY(-2px); }
.contact-socials { display: flex; justify-content: center; gap: 24px; flex-wrap: wrap; }
.social-link {
  font-size: 0.78rem;
  font-weight: 600;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: rgba(255,255,255,0.75);
  border-bottom: 1px solid rgba(255,255,255,0.3);
  padding-bottom: 2px;
  transition: color 0.2s;
}
.social-link:hover { color: var(--green); }

.footer {
  background: var(--black);
  color: var(--white);
  padding: 60px 5% 32px;
}
.footer-grid {
  display: grid;
  grid-template-columns: 1.5fr 1fr 1fr;
  gap: 40px;
  padding-bottom: 48px;
  border-bottom: 1px solid rgba(255,255,255,0.1);
  margin-bottom: 28px;
}
.footer-brand { display: flex; flex-direction: column; gap: 8px; }
.footer-logo-mark { font-size: 1.3rem; color: var(--blue); }
.footer-logo-text {
  font-family: var(--font-display);
  font-size: 1.8rem;
  letter-spacing: 0.1em;
}
.footer-tagline { font-size: 0.78rem; color: rgba(255,255,255,0.4); margin-top: 4px; }
.footer-nav, .footer-socials { display: flex; flex-direction: column; gap: 12px; }
.footer-link {
  font-size: 0.82rem;
  font-weight: 500;
  color: rgba(255,255,255,0.65);
  letter-spacing: 0.08em;
  transition: color 0.2s;
}
.footer-link:hover { color: var(--green); }
.footer-bottom {
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-size: 0.75rem;
  color: rgba(255,255,255,0.35);
}
.footer-made { font-family: var(--font-script); font-size: 0.95rem; color: rgba(255,255,255,0.4); }

@media (max-width: 900px) {
  .hero-content { grid-template-columns: 1fr; }
  .hero-right { align-items: flex-start; }
  .hero-photo-frame { width: 200px; height: 240px; }
  .about-grid { grid-template-columns: 1fr; }
  .toc-grid { grid-template-columns: repeat(2, 1fr); }
  .work-grid { grid-template-columns: 1fr; }
  .work-card-wide { grid-column: span 1; }
  .footer-grid { grid-template-columns: 1fr; }
  .exp-grid { grid-template-columns: 1fr; }
  .about-details-grid { grid-template-columns: 1fr; }
  .nav-links { display: none; }
}
</style>
