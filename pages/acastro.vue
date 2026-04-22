<template>
  <div class="portfolio">

    <!-- NAVBAR -->
    <nav class="navbar" :class="{ scrolled: isScrolled }">

      <!-- Logo — change the href if your homepage URL is different -->
      <a href="/" class="nav-logo">
        <img src="/logo.png" alt="Golem Protocol" class="nav-logo-img" />
        Golem Protocol
      </a>

      <!-- Desktop links (hidden on mobile, see hamburger below) -->
      <ul class="nav-links">
        <li><a href="#about"     @click.prevent="scrollTo('about')">About Me</a></li>
        <li><a href="#skills"    @click.prevent="scrollTo('skills')">Skills</a></li>
        <li><a href="#projects"  @click.prevent="scrollTo('projects')">Projects</a></li>
        <li><a href="#education" @click.prevent="scrollTo('education')">Education</a></li>
      </ul>

    </nav>

    <!-- HERO Section -->
    <section id="home" class="hero">
      <div class="hero-inner">

        <!-- Profile photo -->
        <div class="hero-photo-wrap">
          <img src="/acastro.jpg" alt="Azriel Kaye C. Castro" class="hero-photo" />
        </div>

        <!-- Name + title + buttons -->
        <div class="hero-text">
          <p class="hero-eyebrow">Full Stack Web Developer</p>
          <h1 class="hero-name">Azriel Kaye C. Castro</h1>
          <p class="hero-role">Building elegant solutions to complex problems</p>
          <p class="hero-tagline">Logic meets creativity — one commit at a time.</p>
          <div class="hero-btns">
            <a href="mailto:azrielkayecastro@outlook.com" class="btn btn-primary">📧 Email</a>
            <a href="https://github.com/AzrielKaye" target="_blank" class="btn btn-outline">🔗 GitHub</a>
          </div>
        </div>

      </div>
    </section>


    <!-- ABOUT -->
    <section id="about" class="section bg-white">
      <div class="section-inner">

        <p class="section-label">Who I am</p>
        <h2 class="section-heading">About Me</h2>

        <div class="about-grid">

          <p class="about-text">
            Driven by a passion for building from the ground up, I am a Full Stack Developer
            dedicated to crafting seamless, scalable web experiences. I view every project as
            an opportunity to merge technical logic with creative problem-solving. My approach
            is rooted in a commitment to continuous growth, consistently seeking out new
            frameworks and methodologies to refine my craft and deliver impactful digital solutions.
          </p>

          <div class="stats-grid">
            <div class="stat-box">
              <p class="stat-number">3<span>+</span></p>
              <p class="stat-label">Years Learning</p>
            </div>
            <div class="stat-box">
              <p class="stat-number">8<span>+</span></p>
              <p class="stat-label">Technologies</p>
            </div>
            <div class="stat-box">
              <p class="stat-number">∞</p>
              <p class="stat-label">Curiosity</p>
            </div>
          </div>

        </div>
      </div>
    </section>


    <!-- SKILLS -->
    <section id="skills" class="section bg-paper">
      <div class="section-inner">

        <p class="section-label">What I use</p>
        <h2 class="section-heading">Skills &amp; Technologies</h2>

        <div class="skills-grid">

          <div class="skill-card">
            <p class="skill-icon">🖥️</p>
            <p class="skill-title">Frontend</p>
            <div class="tag-list">
              <span class="tag">Vue.js</span>
              <span class="tag">Nuxt.js</span>
              <span class="tag">React</span>
              <span class="tag">TypeScript</span>
              <span class="tag">Tailwind CSS</span>
            </div>
          </div>

          <div class="skill-card">
            <p class="skill-icon">⚙️</p>
            <p class="skill-title">Backend</p>
            <div class="tag-list">
              <span class="tag">Node.js</span>
              <span class="tag">Java</span>
            </div>
          </div>

          <!-- Skill card: Tools -->
          <div class="skill-card">
            <p class="skill-icon">🛠️</p>
            <p class="skill-title">Tools &amp; Others</p>
            <div class="tag-list">
              <span class="tag">Git</span>
            </div>
          </div>

        </div>
      </div>
    </section>


    <!-- PROJECTS -->
    <section id="projects" class="section bg-dark">
      <div class="section-inner">

        <p class="section-label projects-label">What I've built</p>
        <h2 class="section-heading projects-heading">Featured Projects</h2>

        <div class="projects-grid">

          <div class="project-card">
            <div class="project-top">
              <p class="project-name">Student Task Management Platform</p>
              <span class="project-year">2026</span>
            </div>
            <p class="project-desc">
              A productivity platform that combines note-taking and scheduling
              to keep students on track.
            </p>
            <div class="tag-list">
              <span class="project-tag">Vue.js</span>
              <span class="project-tag">Node.js</span>
              <span class="project-tag">Python</span>
            </div>
          </div>

        </div>
      </div>
    </section>


    <!-- EDUCATION -->
    <section id="education" class="section bg-paper">
      <div class="section-inner">

        <p class="section-label">Background</p>
        <h2 class="section-heading">Education</h2>

        <div class="edu-item">
          <div class="edu-icon">🎓</div>
          <div class="edu-body">
            <p class="edu-degree">Bachelor of Science in Computer Science</p>
            <p class="edu-school">Visayas State University</p>
            <p class="edu-period">2023 — Present</p>
          </div>
        </div>

      </div>
    </section>


    <!-- CONTACT -->
    <section id="contact" class="section bg-white contact-section">
      <div class="section-inner" style="text-align: center;">

        <p class="section-label">Get in touch</p>
        <h2 class="section-heading">Let's Work Together</h2>
        <p class="contact-sub">
          Open to internships, collaborations, and interesting projects. Drop me a message!
        </p>
        <div class="contact-btns">
          <a href="mailto:azrielkayecastro@outlook.com" class="btn btn-primary">📧 azrielkayecastro@outlook.com</a>
          <a href="https://github.com/AzrielKaye" target="_blank" class="btn btn-outline">🔗 GitHub</a>
        </div>

      </div>
    </section>

  </div>
</template>

<script setup lang="ts">
import { ref, onMounted, onUnmounted } from 'vue'

const isScrolled = ref(false)

function handleScroll() {
  isScrolled.value = window.scrollY > 20
}

function scrollTo(sectionId: string) {
  const el = document.getElementById(sectionId)
  if (el) {
    const navHeight = 80
    const elementPosition = el.getBoundingClientRect().top + window.scrollY
    window.scrollTo({
      top: elementPosition - navHeight,
      behavior: 'smooth'
    })
  }
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>


<style scoped>
:root {
  --ink:     #0d0d0d;
  --paper:   #f5f2ec;
  --white:   #ffffff;
  --accent:  #c8432b;
  --accent2: #2b6cc8;
  --muted:   #6b6459;
  --border:  #e0dbd2;
  --radius:  12px;
  --shadow:  0 4px 20px rgba(13, 13, 13, 0.08);
  --nav-h:   80px;
}

/* RESET & BASE */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.portfolio {
  font-family: 'Georgia', serif;
  background: var(--paper);
  color: var(--ink);
  min-height: 100vh;
}

/* NAVBAR */
.navbar {
  position: fixed;
  top: 0; left: 0; right: 0;
  z-index: 100;
  height: var(--nav-h);
  background: rgba(247, 247, 247, 0.92);
  backdrop-filter: blur(20px);
  border-bottom: 1px solid transparent;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 1rem 2.5rem;
  transition: border-color 0.3s, box-shadow 0.2s;
}

.navbar.scrolled {
  box-shadow: 0 10px 30px rgba(53, 48, 48, 0.108);
}

.nav-logo {
  font-family: 'Georgia', serif;
  font-weight: bold;
  font-size: 1.3rem;
  color: var(--ink);
  text-decoration: none;
  letter-spacing: -0.3px;
  padding: 0.45rem 0.9rem;
  border-radius: 6px;
  transition: color 0.2s, background 0.2s;
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.nav-logo-img {
  height: 32px;
  width: auto;
  object-fit: contain;
}

.nav-logo:hover {
  color: var(--ink);
  background: rgb(250, 187, 187);
}

.nav-logo span {
  color: var(--accent); 
}

.nav-links {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  list-style: none;
}

.nav-links a {
  font-size: 0.85rem;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.06em;
  color: var(--muted);
  text-decoration: none;
  padding: 0.45rem 0.9rem;
  border-radius: 6px;
  transition: color 0.2s, background 0.2s;
}

.nav-links a:hover {
  color: var(--ink);
  background: rgb(250, 187, 187);
}


/* HERO SECTION */
.hero {
  min-height: 92vh;
  display: flex;
  align-items: center;
  padding: calc(var(--nav-h) + 4rem) 2.5rem 5rem;
  background: #FFCDC9;
  position: relative;
  overflow: hidden;
}

.hero::before {
  content: '';
  position: absolute;
  inset: 0;
  background-image:
    linear-gradient(var(--border) 1px, transparent 1px),
    linear-gradient(90deg, var(--border) 1px, transparent 1px);
  background-size: 60px 60px;
  opacity: 0.45;
  pointer-events: none; 
}

.hero-inner {
  max-width: 1100px;
  margin: 0 auto;
  width: 100%;
  display: flex;
  align-items: center;
  gap: 4rem;
  position: relative;
  z-index: 1;   
}

/* Profile photo with decorative offset ring */
.hero-photo-wrap {
  flex-shrink: 0;
  position: relative;
}

.hero-photo-wrap::after {
  content: '';
  position: absolute;
  inset: 10px -10px -10px 10px;
  border: 2px solid var(--accent);
  border-radius: 50%;
  z-index: -1;
}

.hero-photo {
  width: 300px;
  height: 300px;
  border-radius: 50%;
  object-fit: cover;
  border: 3px solid var(--ink);
  display: block;
}

.hero-eyebrow {
  font-size: 0.75rem;
  font-weight: 700;
  letter-spacing: 0.14em;
  text-transform: uppercase;
  color: var(--accent);
  margin-bottom: 1rem;
}

.hero-name {
  font-size: clamp(2.4rem, 5vw, 4rem); 
  font-weight: bold;
  line-height: 1.05;
  letter-spacing: -1.5px;
  color: var(--ink);
  margin-bottom: 0.6rem;
}

.hero-role {
  font-size: 1.2rem;
  color: var(--muted);
  margin-bottom: 0.3rem;
}

.hero-tagline {
  font-style: italic;
  font-size: 1rem;
  color: var(--muted);
  margin-bottom: 2rem;
}

.hero-btns {
  display: flex;
  gap: 1rem;
  flex-wrap: wrap;
}


/* BUTTONS */
.btn {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.75rem 1.5rem;
  border-radius: 8px;
  font-size: 0.85rem;
  font-weight: 600;
  text-decoration: none;
  border: 2px solid transparent;
  transition: all 0.25s;
  cursor: pointer;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
}

.btn-primary {
  background: #FFE5E1;
  color: var(--ink);
  border-color: #FFE5E1;
}

.btn-primary:hover {
  background: #FFCDC9;
  border-color: #FFCDC9;
  color: var(--ink);
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
}

.btn-outline {
  background: #FFE5E1;
  color: var(--ink);
  border-color: #FFE5E1;
}

.btn-outline:hover {
  background: #FFCDC9;
  border-color: #FFCDC9;
  color: var(--ink);
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
}


/* SECTIONS */
.section {
  padding: 5rem 2.5rem;
  scroll-margin-top: var(--nav-h);
}

.bg-white  { background: var(--white); border-top: 1px solid var(--border); }
.bg-paper  { background: #FFCDC9; }
.bg-dark   { background: var(--ink); }

.section-inner {
  max-width: 1100px;
  margin: 0 auto;
}

.section-label {
  font-size: 0.72rem;
  font-weight: 700;
  letter-spacing: 0.16em;
  text-transform: uppercase;
  color: var(--accent);
  margin-bottom: 0.75rem;
}

.section-heading {
  font-size: clamp(1.8rem, 3.5vw, 2.8rem);
  font-weight: bold;
  letter-spacing: -1px;
  color: var(--ink);
  margin-bottom: 2.5rem;
  line-height: 1.1;
}


/* ABOUT SECTION */
.about-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  align-items: start;
}

.about-text {
  font-size: 1.1rem;
  line-height: 1.85;
  color: var(--muted);
}

.stats-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1.5rem;
}

.stat-box {
  padding: 2.5rem;
  border: none;
  border-radius: 24px;
  background: var(--white);
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.1);
  transition: box-shadow 0.25s;
}

.stat-box:hover {
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.15);
}

.stat-number {
  font-size: 2rem;
  font-weight: bold;
  color: var(--ink);
  line-height: 1;
  margin-bottom: 0.4rem;
}

.stat-number span {
  color: var(--accent);
}

.stat-label {
  font-size: 0.78rem;
  font-weight: 600;
  color: var(--muted);
  text-transform: uppercase;
  letter-spacing: 0.06em;
}


/* SKILLS SECTION */
.skills-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1.5rem;
}

.skill-card {
  background: var(--white);
  border: none;
  border-radius: 24px;
  padding: 3rem;
  transition: box-shadow 0.25s, transform 0.25s;
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.1);
}

.skill-card:hover {
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.15);
  transform: translateY(-3px);
}

.skill-icon {
  font-size: 1.6rem;
  margin-bottom: 1rem;
}

.skill-title {
  font-size: 0.9rem;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.07em;
  color: var(--ink);
  margin-bottom: 1.25rem;
  font-size: 1.1rem;
}

.tag-list {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
}

.tag {
  display: inline-block;
  padding: 0.6rem 1.2rem;
  color: #000000;
  background: rgba(255, 188, 188, 0.493);
  border: 1px solid rgba(0, 0, 0, 0.949);
  border-radius: 100px;
  font-size: 0.82rem;
  font-weight: 500;
  transition: background 0.2s, color 0.2s, border 0.2s;
  cursor: default;
}

.tag:hover {
  background: var(--ink);
  color: var(--paper);
}


/* PROJECTS SECTION */
.projects-label  { color: #000000; } 
.projects-heading { color: var(--paper); }

.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
  gap: 1.5rem;
}

.project-card {
  background: rgba(255, 255, 255, 0.05);
  border: none;
  border-radius: 30px;
  padding: 3rem;
  transition: box-shadow 0.25s, transform 0.25s;
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.1);
}

.project-card::before {
  content: '';
  position: absolute;
  top: 0; left: 0; right: 0;
  height: 3px;
  background: linear-gradient(90deg, var(--accent), var(--accent2));
}

.project-card:hover {
  background: rgba(255, 255, 255, 0.09);
  transform: translateY(-4px);
}

.project-top {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: 1rem;
}

.project-name {
  font-size: 1.2rem;
  font-weight: bold;
  color: var(--paper);
  flex: 1;
  margin-right: 1rem;
  line-height: 1.3;
}

.project-year {
  font-size: 0.75rem;
  font-weight: 700;
  color: #000000;
  background: rgba(255, 188, 188, 0.493);
  border: 1px solid rgba(0, 0, 0, 0.949);
  padding: 0.25rem 0.7rem;
  border-radius: 100px;
  white-space: nowrap;
}

.project-desc {
  font-size: 0.92rem;
  color: black;
  line-height: 1.7;
  margin-bottom: 1.25rem;
}

.project-tag {
  display: inline-block;
  padding: 0.3rem 0.75rem;
  font-size: 0.78rem;
  font-weight: 600;
  color: #000000;
  background: rgba(255, 188, 188, 0.493);
  border: 1px solid rgba(0, 0, 0, 0.949);
  border-radius: 100px;
}


/* EDUCATION SECTION */
.edu-item {
  display: flex;
  align-items: flex-start;
  gap: 2rem;
  padding: 3rem;
  border: none;
  border-radius: 24px;
  background: var(--white);
  transition: box-shadow 0.25s, transform 0.25s;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.12);
}

.edu-item:hover {
  box-shadow: 0 12px 40px rgba(0, 0, 0, 0.18);
  transform: translateY(-2px);
}

.edu-icon {
  width: 52px;
  height: 52px;
  border-radius: 12px;
  background: var(--ink);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.4rem;
  flex-shrink: 0;
}

.edu-degree {
  font-size: 1.05rem;
  font-weight: bold;
  color: var(--ink);
  margin-bottom: 0.25rem;
}

.edu-school {
  font-size: 0.95rem;
  color: var(--muted);
  margin-bottom: 0.3rem;
}

.edu-period {
  font-size: 0.78rem;
  font-weight: 700;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: var(--accent);
}


/* CONTACT SECTION */
.contact-section {
  border-top: 1px solid var(--border);
}

.contact-sub {
  font-size: 1.1rem;
  color: var(--muted);
  max-width: 500px;
  margin: 0 auto 2.5rem;
}

.contact-btns {
  display: flex;
  justify-content: center;
  gap: 1rem;
  flex-wrap: wrap;
}

</style>