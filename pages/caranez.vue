<script lang="ts"></script>
<template>
    <client-only>
        <nav class="navbar">
            <div class="nav-blur"></div>
            <div class="nav-container">
                <div class="left">
                    <a href="/" class="home">
                        <img src="/logo.png" width=20 height=20 class="gpLogo">
                        <span>Golem Protocol</span>
                    </a>
                </div>
                
                <div class="right">
                    <a href="#about" class="nav-link" @click.prevent="scrollToSection('about')">
                        <i class="fa-regular fa-user"></i>
                        <span>About</span>
                    </a>
                    <a href="#education" class="nav-link" @click.prevent="scrollToSection('education')">
                        <i class="fa-solid fa-graduation-cap"></i>
                        <span>Education</span>
                    </a>
                    <a href="#projects" class="nav-link" @click.prevent="scrollToSection('projects')">
                        <i class="fa-regular fa-folder-open"></i>
                        <span>Projects</span>
                    </a>
                    <a href="#skills" class="nav-link" @click.prevent="scrollToSection('skills')">
                        <i class="fa-solid fa-code"></i>
                        <span>Skills</span>
                    </a>
                    <a href="#achievements" class="nav-link" @click.prevent="scrollToSection('achievements')">
                        <i class="fa-solid fa-trophy"></i>
                        <span>Achievements</span>
                    </a>
                </div>
            </div>
            
            <!-- Animated border bottom -->
            <div class="nav-border"></div>
        </nav>

        <main>  
            <h1 id="about" class="header">ABOUT ME</h1>
            <section class="hero reveal">
                <div class="hero-container">
                    <img src="../public/carl.jpg" alt="Carl Photo" class="hero-image">
                    <h1 class="name">Carl Roy F. Arañez</h1>
                    
                    <div class="contacts-container">
                        <a href="https://github.com/CaptainKaru" class="icon"><i class="fa-brands fa-github fa-2x"></i> Github</a>
                        <a href="#" @click.prevent="openEmailModal" class="icon"><i class="fa-solid fa-envelope fa-2x"></i> Email</a>
                    </div>
                </div>

                <div class="hero-content">
                    <p>
                        Hi, I'm Carl! 👋 I'm a Computer Science student with a passion for front-end development. I enjoy building clean, responsive, and visually engaging web experiences — turning ideas into products people actually enjoy using.
                        I'm always learning, whether it's picking up a new framework, refining my design sense, or writing better code. I pay close attention to detail and take pride in the work I put out. Feel free to look around, and don't hesitate to reach out — I'm always open to opportunities and connections!
                    </p>
                </div>
            </section>

            <br>
            <h1 id="education" class="header"> EDUCATIONAL BACKGROUND</h1>
            <br>
            
            <section class="education reveal">
                <div class="education-content">
                    <div class="logo-container">
                        <a href="https://www.vsu.edu.ph/" target="_blank" rel="noopener noreferrer">
                            <img src="../public/vsu.png" alt="VSU Logo" class="vsu-logo">
                        </a>
                        <div class="divider"></div>
                        <a href="https://www.facebook.com/vsufc/" target="_blank" rel="noopener noreferrer">
                            <img src="../public/foc.png" alt="FOC Logo" class="foc-logo">
                        </a>
                    </div>
                    <p>
                        I am currently an undergraduate student at the <span class="vsu-text">Visayas State University</span> 
                        under the <span class="foc-text">Faculty of Computing</span>, pursuing a degree in 
                        Computer Science. <span class="year">(2024 - Present)</span>
                    </p>
                </div>
            </section>

            <br>
            <h1 id="projects" class="header">Projects</h1>
            <br>

            <section class="projects reveal">
                <div class="project">
                    <div class="project-icon">
                        <i class="fa-solid fa-code"></i>
                    </div>
                    <div class="project-header">
                        <h1>Student Management System</h1>
                        <div class="project-meta">
                            <span class="tech-stack"><i class="fa-solid fa-layer-group"></i> C++, SQL</span>
                            <span class="role"><i class="fa-solid fa-user"></i> Fullstack Developer</span>
                            <span class="date"><i class="fa-regular fa-calendar"></i> Nov. 2026 - Dec. 2026</span>
                        </div>
                    </div>
                    <ul class="project-list">
                        <li>Developed a full-stack application managing 30+ student records, automating grade calculations that previously required 15+ minutes of manual work per report.</li>
                        <li>Engineered 8+ optimized SQL queries with joins and aggregates, reducing data processing time by approximately 75% for batch operations.</li>
                        <li>Designed an intuitive CLI with a structured 5-menu navigation system, decreasing user input errors through guided prompts and validation.</li>
                    </ul>
                    <div class="project-glow"></div>
                </div>     
                
                <div class="project">
                    <div class="project-icon">
                        <i class="fa-solid fa-pen-ruler"></i>
                    </div>
                    <div class="project-header">
                        <h1>"EcoBayan" Platform Prototype</h1>
                        <div class="project-meta">
                            <span class="tech-stack"><i class="fa-brands fa-figma"></i> Figma</span>
                            <span class="role"><i class="fa-solid fa-palette"></i> UI/UX Designer</span>
                            <span class="date"><i class="fa-regular fa-calendar"></i> June 8 - June 10, 2025</span>
                        </div>
                    </div>
                    <ul class="project-list">
                        <li>Co-designed a 12-screen, high-fidelity prototype that defined the visual language and component library for a recycling platform.</li>
                        <li>Mapped 4 comprehensive user journeys (reporting, rewards, education, navigation), reducing hypothetical user task completion time by streamlining flows.</li>
                        <li>The user-centered design and clear information architecture were pivotal in winning 1st Place against 10+ competing teams.</li>
                    </ul>
                    <div class="project-glow"></div>
                </div>
            </section>

            <br>
            <h1 id="skills" class="header">Skills</h1>
            <br>

            <section class="skills reveal">
                <div class="skills-container">
                    <div class="skill-category">
                        <h2>Languages</h2>
                        <div class="skills-grid">
                            <div class="skill-item">
                                <i class="fa-brands fa-cuttlefish fa-2x"></i>
                                <span>C++</span>
                            </div>
                            <div class="skill-item">
                                <i class="fa-brands fa-java fa-2x"></i>
                                <span>Java</span>
                            </div>
                            <div class="skill-item">
                                <i class="fa-brands fa-js fa-2x"></i>
                                <span>JavaScript</span>
                            </div>
                            <div class="skill-item">
                                <i class="fa-brands fa-css3-alt fa-2x"></i>
                                <span>CSS</span>
                            </div>
                            <div class="skill-item">
                                <i class="fa-brands fa-html5 fa-2x"></i>
                                <span>HTML</span>
                            </div>
                        </div>
                    </div>
                    
                    <div class="skill-category">
                        <h2>Frameworks & Libraries</h2>
                        <div class="skills-grid">
                            <div class="skill-item">
                                <i class="fa-brands fa-node fa-2x"></i>
                                <span>Node.js</span>
                            </div>
                            <div class="skill-item">
                                <i class="fa-brands fa-react fa-2x"></i>
                                <span>React</span>
                            </div>
                            <div class="skill-item">
                                <i class="fa-brands fa-vuejs fa-2x"></i>
                                <span>Nuxt</span>
                            </div>
                        </div>
                    </div>
                </div>
            </section>

            <br>
            <h1 class="header">Achievements</h1>
            <br>

            <section id="achievements" class="achievements reveal">
                <div class="achievement-card">
                <div class="achievement-icon">
                    <i class="fa-solid fa-trophy fa-3x"></i>
                </div>
                <div class="achievement-details">
                    <h2>1st Place – IDEA + Reverse Pitching Competition</h2>
                    <h3>2025 Regional Smart Communities Exposition (RSCENE)</h3>
                    <p class="achievement-date">
                        <i class="fa-regular fa-calendar"></i> June 15-18, 2025 | Catbalogan City, Samar
                    </p>
                    <p class="achievement-description">
                        Contributed to the "Siklo Squad" team in developing a digital platform that improves waste management 
                        through community-driven recycling, earning the highest score for usability, relevance, 
                        and potential to create real environmental change.
                    </p>
                    <div class="achievement-tags">
                        <span class="tag">UI/UX Design</span>
                        <span class="tag">Climate Tech</span>
                        <span class="tag">Waste Management</span>
                    </div>
                    <a href="https://www.vsu.edu.ph/articles/news/2739-vsu-computer-science-students-sweep-top-awards-at-regional-tech-and-innovation-event" 
                    target="_blank" class="read-more-btn">
                        Read Full Article <i class="fa-solid fa-arrow-right"></i>
                    </a>
                </div>
            </div>
            </section>
        </main>  

        <Cookies />

        <!-- Email Modal -->
        <div v-if="isEmailModalOpen" class="modal-overlay" @click="closeEmailModal">
            <div class="modal-content" @click.stop>
                <button class="modal-close" @click="closeEmailModal">&times;</button>
                
                <h2>Send me a message</h2>
                <p class="email-display">
                    Send email to: <strong>carlroy.aranez02@gmail.com</strong>
                </p>
                
                <div class="message-box">
                    <p class="info-text">
                        ℹ️ To send an email, you'll need to use your email client.
                    </p>
                    <p class="info-text">
                        Click the button below to open Gmail:
                    </p>
                    
                    <a href="https://mail.google.com/mail/?view=cm&fs=1&to=carlroy.aranez02@gmail.com" target="_blank" class="email-btn">
                        <i class="fa-brands fa-google"></i> Open Gmail
                    </a>
                    
                    <div class="alternative-text">
                        <p>Or just copy my email:</p>
                        <div class="copy-container">
                            <span class="copy-email">carlroy.aranez02@gmail.com</span>
                            <button @click="copyEmail" class="copy-btn">Copy</button>
                        </div>
                    </div>
                    
                    <div v-if="copySuccess" class="copy-success">
                        ✓ Email copied to clipboard!
                    </div>
                </div>
            </div>
        </div>
    </client-only>
</template>

<script setup lang="ts">
    import { useSeoMeta, useHead } from '@vueuse/head';
    import { onMounted, ref } from 'vue';

    const title = "Project Golem | Terms of Service";
    const description = "Review the Living Machine AI Terms of Service with data protection, account, and compliance details for GDPR and Philippine law.";

    useSeoMeta({
        title: () => title,
        description: () => description,
        charset: "utf-8",
        viewport: "width=device-width, initial-scale=1.0"
    });

    useHead({
        link: [
            { rel: 'icon', type: 'image/png', href: '/logo.png' },
            { rel: 'stylesheet', href: '/reset.css' },
            { rel: 'stylesheet', href: '/custom.css' },
            { rel: 'preconnect', href: 'https://fonts.googleapis.com' },
            { rel: 'preconnect', href: 'https://fonts.gstatic.com', crossorigin: '' },
            { rel: 'stylesheet', href: 'https://fonts.googleapis.com/css2?family=Bitcount:wght@100..900&family=Roboto:ital,wght@0,100..900;1,100..900&display=swap' },
            { rel: 'stylesheet', href: 'https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css' }
        ]
    });

    defineProps<{
    navAdminMode: string;
    bgColor?: string;
    }>();


    
    const isEmailModalOpen = ref(false)
    const copySuccess = ref(false)

    const openEmailModal = () => {
        isEmailModalOpen.value = true
        // Save the current scrollbar width and add padding
        const scrollbarWidth = window.innerWidth - document.documentElement.clientWidth
        document.body.style.overflow = 'hidden'
        document.body.style.paddingRight = `${scrollbarWidth}px`
        copySuccess.value = false
    }

    const closeEmailModal = () => {
        isEmailModalOpen.value = false
        document.body.style.overflow = ''
        document.body.style.paddingRight = ''
    }

    const copyEmail = async () => {
        try {
            await navigator.clipboard.writeText('carlroy.aranez02@gmail.com')
            copySuccess.value = true
            setTimeout(() => {
                copySuccess.value = false
            }, 2000)
        } catch (err) {
            console.error('Failed to copy:', err)
        }
    }

    const scrollToSection = (sectionId: string) => {
        const element = document.getElementById(sectionId)
        if (element) {
            const offset = 100 // Adjust this number (try 80, 100, 120, 150)
            const elementPosition = element.getBoundingClientRect().top
            const offsetPosition = elementPosition + window.pageYOffset - offset
            
            window.scrollTo({
                top: offsetPosition,
                behavior: 'smooth'
            })
        }
    }

    onMounted(() => {
        // Close modal with Escape key
        window.addEventListener('keydown', (e) => {
            if (e.key === 'Escape' && isEmailModalOpen.value) {
                closeEmailModal()
            }
        })
        
        setTimeout(() => {
            document.querySelectorAll('.reveal').forEach(el => {
                el.classList.remove('visible')
            })
            
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(el => {
                    if (el.isIntersecting) {
                        el.target.classList.add('visible')
                    } else {
                        el.target.classList.remove('visible')
                    }
                })
            }, { threshold: 0.1 })

            document.querySelectorAll('.reveal').forEach(el => observer.observe(el))
        }, 100)
    })
</script>

<style>
:root {
    --primary-color: #37353E;
    --secondary-color: #44444E;
    --tertiary-color: #EEDF7A;
    --text-color: #D3DAD9;
}

.reveal {
  opacity: 0;
  transform: translateY(30px);
  transition: opacity 0.6s ease, transform 0.6s ease;
}

.reveal.visible {
  opacity: 1;
  transform: translateY(0);
}
</style>

<style scoped>
main {
    background: linear-gradient(135deg, #2a2830 0%, #37353E 25%, #2a2830 50%, #37353E 75%, #2a2830 100%);
    background-size: 200% 200%;
    animation: meshGradient 15s ease infinite;
    height: auto;
    padding-top: 80px;
    display: flex;
    flex-direction: column;
    gap: 20px;
    position: relative;
}

@keyframes meshGradient {
    0% {
        background-position: 0% 50%;
    }
    50% {
        background-position: 100% 50%;
    }
    100% {
        background-position: 0% 50%;
    }
}

main::before {
    content: '';
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-image: radial-gradient(rgba(238, 223, 122, 0.08) 1px, transparent 1px);
    background-size: 40px 40px;
    pointer-events: none;
    z-index: 0;
}

main > * {
    position: relative;
    z-index: 1;
}

@keyframes fadeInPage {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes fadeIn {
    from { opacity: 0; }
    to { opacity: 1; }
}

@keyframes slideIn {
    from {
        transform: translateY(-50px);
        opacity: 0;
    }
    to {
        transform: translateY(0);
        opacity: 1;
    }
}

main .header {
    text-align: center;
    font-size: 2.5em;
    color: var(--text-color);
    margin-bottom: 30px;
    position: relative;
    display: inline-block;
    width: 100%;
}

main .header::after {
    content: '';
    position: absolute;
    bottom: -10px;
    left: 50%;
    transform: translateX(-50%);
    width: 60px;
    height: 3px;
    background: var(--tertiary-color);
    border-radius: 2px;
    transition: width 0.3s ease;
}

main .header:hover::after {
    width: 100px;
}

.modal-overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.8);
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 10000;
    animation: fadeIn 0.3s ease;
}

.modal-content {
    background: linear-gradient(135deg, var(--secondary-color), var(--primary-color));
    padding: 30px;
    border-radius: 20px;
    max-width: 450px;
    width: 90%;
    position: relative;
    color: var(--text-color);
    animation: slideIn 0.3s ease;
    border: 1px solid rgba(238, 223, 122, 0.2);
}

.modal-close {
    position: absolute;
    top: 15px;
    right: 20px;
    font-size: 28px;
    background: none;
    border: none;
    color: var(--text-color);
    cursor: pointer;
    transition: all 0.3s ease;
}

.modal-close:hover {
    color: var(--tertiary-color);
    transform: rotate(90deg);
}

.email-display {
    margin: 20px 0;
    text-align: center;
    font-size: 1.1em;
}

.message-box {
    margin-top: 20px;
    text-align: center;
}

.info-text {
    margin: 10px 0;
    font-size: 0.95em;
    opacity: 0.9;
}

.email-btn {
    display: inline-flex;
    align-items: center;
    gap: 10px;
    background-color: var(--tertiary-color);
    color: var(--primary-color);
    padding: 12px 24px;
    margin: 15px 0;
    border-radius: 8px;
    text-decoration: none;
    font-weight: bold;
    transition: all 0.3s ease;
}

.email-btn:hover {
    transform: scale(1.05);
    box-shadow: 0 5px 15px rgba(238, 223, 122, 0.3);
}

.alternative-text {
    margin-top: 15px;
    font-size: 0.9em;
}

.copy-container {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 10px;
    margin-top: 10px;
}

.copy-email {
    background-color: var(--primary-color);
    padding: 8px 12px;
    border-radius: 5px;
    font-family: monospace;
    font-size: 0.9em;
}

.copy-btn {
    background-color: var(--tertiary-color);
    color: var(--primary-color);
    border: none;
    padding: 8px 15px;
    border-radius: 5px;
    cursor: pointer;
    font-weight: bold;
    transition: all 0.2s ease;
}

.copy-btn:hover {
    transform: scale(1.05);
    box-shadow: 0 2px 8px rgba(238, 223, 122, 0.3);
}

.copy-success {
    margin-top: 15px;
    padding: 10px;
    background-color: #4CAF50;
    color: white;
    border-radius: 5px;
    animation: fadeIn 0.3s ease;
}

/* ===== NAVBAR ===== */
.navbar {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 70px;
    z-index: 7000;
    backdrop-filter: blur(10px);
    background: rgba(55, 53, 62, 0.85);
    border-bottom: 1px solid rgba(238, 223, 122, 0.1);
}

.nav-blur {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(135deg, rgba(68, 68, 78, 0.9), rgba(55, 53, 62, 0.95));
    backdrop-filter: blur(20px);
    z-index: -1;
}

.nav-container {
    max-width: 1400px;
    margin: 0 auto;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 0 0 5%;
    position: relative;
}

.nav-border {
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    height: 2px;
    background: linear-gradient(90deg, 
        transparent, 
        var(--tertiary-color), 
        var(--tertiary-color), 
        transparent);
    transform: scaleX(0);
    transition: transform 0.5s ease;
}

.navbar:hover .nav-border {
    transform: scaleX(1);
}

.left {
    display: flex;
    align-items: center;
}

.home {
    display: flex;
    align-items: center;
    gap: 12px;
    padding: 8px 20px;
    font-family: "Bitcount", "Roboto", Arial, serif;
    font-size: 1.1em;
    text-decoration: none;
    border-radius: 40px;
    color: var(--text-color);
    transition: all 0.3s ease;
}

.home:hover {
    transform: translateY(-2px);
    color: var(--tertiary-color);
}

.gpLogo {
    width: 24px;
    height: 24px;
    transition: transform 0.3s ease;
}

.home:hover .gpLogo {
    transform: rotate(5deg) scale(1.05);
}

.right {
    display: flex;
    align-items: center;
    gap: 8px;
}

.nav-link {
    display: flex;
    align-items: center;
    gap: 8px;
    padding: 8px 18px;
    color: var(--text-color);
    text-decoration: none;
    font-size: 0.9em;
    font-weight: 500;
    border-radius: 40px;
    transition: all 0.3s ease;
    position: relative;
}

.nav-link i {
    font-size: 1em;
    transition: all 0.3s ease;
}

.nav-link:hover i {
    transform: scale(1.1);
}

.nav-link span {
    transition: transform 0.2s ease;
}

.nav-link:hover span {
    transform: translateX(3px);
}

.nav-link::before {
    content: '';
    position: absolute;
    bottom: 0;
    left: 50%;
    transform: translateX(-50%);
    width: 0;
    height: 2px;
    background: var(--tertiary-color);
    transition: width 0.3s ease;
}

.nav-link:hover::before {
    width: 60%;
}

.nav-link:hover {
    background: rgba(238, 223, 122, 0.1);
    color: var(--tertiary-color);
    transform: translateY(-2px);
}

/* Mobile responsive */
@media (max-width: 900px) {
    .nav-link span {
        display: none;
    }
    
    .nav-link i {
        font-size: 1.2em;
    }
    
    .nav-link {
        padding: 8px 12px;
    }
}

@media (max-width: 600px) {
    .home span {
        display: none;
    }
    
    .home {
        padding: 8px 12px;
    }
    
    .nav-link {
        padding: 8px 10px;
    }
    
    .right {
        gap: 4px;
    }
}

/* Hover effect for the whole navbar */
@keyframes navGlow {
    0% {
        box-shadow: 0 2px 10px rgba(0, 0, 0, 0.2);
    }
    100% {
        box-shadow: 0 2px 20px rgba(238, 223, 122, 0.15);
    }
}

.navbar:hover {
    animation: navGlow 0.3s ease forwards;
}

/* ===== MAIN PAGE ===== */
main {
    background-color: var(--primary-color);
    height: auto;
    padding-top: 80px;
    display: flex;
    flex-direction: column;
    gap: 20px;
}

section {
    margin: 0px 100px 0 100px;
    box-shadow: 0 0 30px 10px rgba(0, 0, 0, 0.5);
    background: linear-gradient(135deg, rgba(68, 68, 78, 0.95), rgba(55, 53, 62, 0.98));
    border-radius: 20px;
    height: auto;
    padding: 20px 150px 20px 150px;
    display: flex;
    gap: 200px;
    color: var(--text-color);
    margin-bottom: 50px;
    border: 1px solid rgba(238, 223, 122, 0.1);
    transition: box-shadow 0.4s cubic-bezier(0.4, 0, 0.2, 1), border-color 0.3s ease;
    position: relative;
    overflow: hidden;
}

section:hover {
    border-color: rgba(238, 223, 122, 0.3);
    box-shadow: 0 20px 40px rgba(0, 0, 0, 0.5);
}

/* Section glow effect */
section::before {
    content: '';
    position: absolute;
    top: 0;
    left: -100%;
    width: 100%;
    height: 100%;
    background: linear-gradient(90deg, transparent, rgba(238, 223, 122, 0.08), transparent);
    transition: left 0.6s ease;
    pointer-events: none;
}

section:hover::before {
    left: 100%;
}

/* ===== HERO SECTION ===== */
.hero {
    min-height: 65vh;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 150px;
}

.hero-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    gap: 20px;
    flex-shrink: 0;
}

.hero-image {
    width: 220px;
    height: 220px;
    border-radius: 50%;
    object-fit: cover;
    border: 3px solid var(--primary-color);
    box-shadow: 0 0 20px rgba(0, 0, 0, 0.3);
    transition: all 0.3s ease;
}

.hero-image:hover {
    transform: scale(1.05) rotate(3deg);
    box-shadow: 0 0 30px rgba(238, 223, 122, 0.3);
}

.name {
    font-family: 'Bitcount', sans-serif;
    font-size: 1.5em;
    font-weight: 400;
    color: var(--text-color);
    border-bottom: 2px solid var(--tertiary-color);
    padding-bottom: 10px;
    white-space: nowrap;
}

.contacts-container {
    display: flex;
    gap: 15px;
    margin-top: 5px;
}

.icon {
    display: flex;
    align-items: center;
    gap: 8px;
    padding: 8px 16px;
    color: var(--text-color);
    text-decoration: none;
    border-radius: 8px;
    transition: all 0.3s ease;
}

.icon:hover {
    color: var(--tertiary-color);
    transform: translateY(-3px);
    background: rgba(238, 223, 122, 0.1);
}

.hero-content {
    max-width: 550px;
    flex: 1;
}

.hero-content p {
    text-align: justify;
    font-size: 1em;
    line-height: 1.6;
    color: var(--text-color);
    opacity: 0.9;
    margin: 0;
}

/* ===== EDUCATIONAL BACKGROUND ===== */
.education-content {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 8em;
    width: 100%;
}

.logo-container {
    display: flex;
    align-items: center;
    gap: 30px;
}

.divider {
    width: 2px;
    height: 150px;
    background-color: var(--tertiary-color);
    transition: all 0.3s ease;
}

.logo-container img {
    width: 180px;
    height: 180px;
    border-radius: 50%;
    object-fit: cover;
    transition: all 0.3s ease;
    box-shadow: 0 0 15px rgba(0, 0, 0, 0.3);
}

.vsu-logo:hover {
    transform: scale(1.08);
    box-shadow: 0 0 30px rgba(0, 131, 35, 0.6);
}

.foc-logo:hover {
    transform: scale(1.08);
    box-shadow: 0 0 30px rgba(0, 180, 240, 0.6);
}

.education-content p {
    max-width: 500px;
    font-size: 1.1em;
    line-height: 1.6;
    text-align: justify;
    color: var(--text-color);
    transition: transform 0.3s ease;
}

.vsu-text {
    color: #4CAF50;
    font-weight: 500;
    transition: all 0.3s ease;
}

.vsu-text:hover {
    text-shadow: 0 0 8px rgba(76, 175, 80, 0.5);
}

.foc-text {
    color: rgb(0, 180, 240);
    font-weight: 500;
    transition: all 0.3s ease;
}

.foc-text:hover {
    text-shadow: 0 0 8px rgba(0, 180, 240, 0.5);
}

.year {
    color: var(--tertiary-color);
    font-weight: 500;
    white-space: nowrap;
}

/* ===== PROJECTS SECTION ===== */
main .projects {
    display: flex;
    flex-direction: column;
    gap: 50px;
}

.project {
    position: relative;
    background: linear-gradient(135deg, rgba(68, 68, 78, 0.95), rgba(55, 53, 62, 0.98));
    border-radius: 20px;
    padding: 35px;
    transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
    overflow: hidden;
    border: 1px solid rgba(238, 223, 122, 0.1);
}

.project:hover {
    transform: translateY(-8px);
    border-color: rgba(238, 223, 122, 0.3);
    box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
}

.project-glow {
    position: absolute;
    top: 0;
    left: -100%;
    width: 100%;
    height: 100%;
    background: linear-gradient(90deg, transparent, rgba(238, 223, 122, 0.1), transparent);
    transition: left 0.6s ease;
    pointer-events: none;
}

.project:hover .project-glow {
    left: 100%;
}

.project-icon {
    position: absolute;
    top: 30px;
    right: 30px;
    font-size: 2.5em;
    color: var(--tertiary-color);
    opacity: 0.3;
    transition: all 0.3s ease;
}

.project:hover .project-icon {
    opacity: 0.8;
    transform: scale(1.1) rotate(5deg);
}

.project-header h1 {
    font-size: 1.8em;
    margin-bottom: 15px;
    color: var(--tertiary-color);
    position: relative;
    display: inline-block;
}

.project-header h1::before {
    content: '';
    position: absolute;
    bottom: -5px;
    left: 0;
    width: 40px;
    height: 2px;
    background: var(--tertiary-color);
    transition: width 0.3s ease;
}

.project:hover .project-header h1::before {
    width: 80px;
}

.project-meta {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    margin-bottom: 20px;
}

.project-meta span {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    font-size: 0.85em;
    padding: 5px 12px;
    background: rgba(238, 223, 122, 0.1);
    border-radius: 20px;
    color: var(--text-color);
    transition: all 0.3s ease;
}

.project-meta span:hover {
    background: rgba(238, 223, 122, 0.2);
    transform: translateY(-2px);
}

.project-meta i {
    color: var(--tertiary-color);
    font-size: 0.9em;
}

.project-list {
    list-style: none;
    padding: 0;
    margin: 0;
}

.project-list li {
    padding: 10px 0 10px 28px;
    margin-bottom: 8px;
    line-height: 1.5;
    position: relative;
    transition: transform 0.2s ease;
}

.project-list li:hover {
    transform: translateX(5px);
}

.project-list li::before {
    content: "✦";
    position: absolute;
    left: 0;
    color: var(--tertiary-color);
    font-size: 1.1em;
    transition: transform 0.2s ease;
}

.project-list li:hover::before {
    transform: rotate(90deg);
}

/* ===== SKILLS SECTION ===== */
.skills {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 40px 60px !important;
}

.skills-container {
    display: flex;
    flex-direction: row;
    gap: 100px;
    justify-content: center;
    flex-wrap: wrap;
    width: 100%;
}

.skill-category {
    text-align: center;
    flex: 1;
    min-width: 200px;
}

.skill-category h2 {
    color: var(--tertiary-color);
    font-size: 1.5em;
    margin-bottom: 25px;
    border-bottom: 2px solid var(--tertiary-color);
    display: inline-block;
    padding-bottom: 8px;
    transition: all 0.3s ease;
}

.skill-category h2:hover {
    letter-spacing: 2px;
    border-bottom-color: var(--text-color);
}

.skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
    gap: 20px;
    justify-items: center;
    align-items: center;
}

.skill-item {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 10px;
    padding: 15px;
    background: linear-gradient(135deg, rgba(55, 53, 62, 0.9), rgba(68, 68, 78, 0.9));
    border-radius: 15px;
    transition: all 0.3s ease;
    width: 100%;
    max-width: 100px;
    border: 1px solid rgba(238, 223, 122, 0.1);
}

.skill-item:hover {
    transform: translateY(-8px) scale(1.05);
    box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
    border-color: rgba(238, 223, 122, 0.3);
}

.skill-item i {
    color: var(--tertiary-color);
    transition: all 0.3s ease;
}

.skill-item:hover i {
    transform: scale(1.1);
    text-shadow: 0 0 10px rgba(238, 223, 122, 0.5);
}

.skill-item span {
    color: var(--text-color);
    font-size: 0.9em;
    font-weight: 500;
}

/* ===== ACHIEVEMENTS SECTION ===== */
.achievements {
    display: flex;
    flex-direction: column;
    gap: 30px;
    padding: 40px 60px !important;
}

.achievement-card {
    position: relative;
    display: flex;
    gap: 30px;
    background: linear-gradient(135deg, rgba(68, 68, 78, 0.95), rgba(55, 53, 62, 0.98));
    border-radius: 20px;
    padding: 35px;
    transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
    overflow: hidden;
    border: 1px solid rgba(238, 223, 122, 0.1);
}

.achievement-card:hover {
    transform: translateY(-8px);
    border-color: rgba(238, 223, 122, 0.3);
    box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
}

.achievement-glow {
    position: absolute;
    top: 0;
    left: -100%;
    width: 100%;
    height: 100%;
    background: linear-gradient(90deg, transparent, rgba(238, 223, 122, 0.1), transparent);
    transition: left 0.6s ease;
    pointer-events: none;
}

.achievement-card:hover .achievement-glow {
    left: 100%;
}

.achievement-icon {
    flex-shrink: 0;
    background: linear-gradient(135deg, var(--tertiary-color), #d4c45a);
    width: 85px;
    height: 85px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    color: var(--primary-color);
    transition: all 0.3s ease;
    position: relative;
    z-index: 1;
}

.achievement-card:hover .achievement-icon {
    transform: scale(1.05) rotate(5deg);
    box-shadow: 0 0 20px rgba(238, 223, 122, 0.4);
}

.achievement-details {
    flex: 1;
    position: relative;
    z-index: 1;
}

.achievement-details h2 {
    font-size: 1.6em;
    margin-bottom: 12px;
    color: var(--tertiary-color);
    position: relative;
    display: inline-block;
}

.achievement-details h2::before {
    content: '';
    position: absolute;
    bottom: -5px;
    left: 0;
    width: 40px;
    height: 2px;
    background: var(--tertiary-color);
    transition: width 0.3s ease;
}

.achievement-card:hover .achievement-details h2::before {
    width: 80px;
}

.achievement-meta {
    display: flex;
    flex-wrap: wrap;
    gap: 20px;
    margin-bottom: 20px;
}

.achievement-meta span {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    font-size: 0.85em;
    padding: 5px 12px;
    background: rgba(238, 223, 122, 0.1);
    border-radius: 20px;
    color: var(--text-color);
    transition: all 0.3s ease;
}

.achievement-meta span:hover {
    background: rgba(238, 223, 122, 0.2);
    transform: translateY(-2px);
}

.achievement-meta i {
    color: var(--tertiary-color);
    font-size: 0.9em;
}

.achievement-description {
    color: var(--text-color);
    line-height: 1.6;
    margin-bottom: 20px;
    font-size: 0.95em;
    opacity: 0.9;
    transition: transform 0.2s ease;
}

.achievement-card:hover .achievement-description {
    transform: translateX(3px);
}

.achievement-tags {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
    margin-bottom: 25px;
}

.tag {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    background-color: rgba(238, 223, 122, 0.1);
    color: var(--tertiary-color);
    padding: 6px 14px;
    border-radius: 20px;
    font-size: 0.85em;
    font-weight: 500;
    transition: all 0.3s ease;
}

.tag:hover {
    background-color: rgba(238, 223, 122, 0.2);
    transform: translateY(-2px);
}

.tag i {
    font-size: 0.85em;
}

.read-more-btn {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    color: var(--tertiary-color);
    text-decoration: none;
    font-weight: 500;
    transition: all 0.3s ease;
    padding: 8px 0;
    position: relative;
}

.read-more-btn::after {
    content: '';
    position: absolute;
    bottom: 0;
    left: 0;
    width: 0;
    height: 1px;
    background: var(--tertiary-color);
    transition: width 0.3s ease;
}

.read-more-btn:hover {
    gap: 12px;
}

.read-more-btn:hover::after {
    width: 100%;
}

/* ===== RESPONSIVE DESIGN ===== */
@media (max-width: 1200px) {
    section {
        margin: 0px 50px 0 50px;
        padding: 20px 80px 20px 80px;
        gap: 100px;
    }
    
    .hero {
        gap: 80px;
    }
}

@media (max-width: 968px) {
    section {
        margin: 0px 30px 0 30px;
        padding: 20px 40px 20px 40px;
        gap: 50px;
        flex-direction: column;
    }
    
    .hero {
        flex-direction: column;
        text-align: center;
    }
    
    .hero-content p {
        text-align: center;
    }
    
    .education-content {
        flex-direction: column;
        gap: 30px;
    }
    
    .logo-container {
        flex-direction: column;
    }
    
    .divider {
        width: 150px;
        height: 2px;
    }
    
    .logo-container:hover .divider {
        width: 180px;
        height: 2px;
    }
    
    .skills-container {
        flex-direction: column;
        gap: 50px;
    }
    
    .project-icon {
        position: relative;
        top: auto;
        right: auto;
        text-align: center;
        margin-bottom: 15px;
        opacity: 0.6;
    }
    
    .project-meta {
        flex-direction: column;
        gap: 10px;
    }
    
    .project-header h1 {
        text-align: center;
        display: block;
    }
    
    .project-header h1::before {
        left: 50%;
        transform: translateX(-50%);
    }
    
    .achievement-card {
        flex-direction: column;
        align-items: center;
        text-align: center;
    }
    
    .achievement-details h2::before {
        left: 50%;
        transform: translateX(-50%);
    }
    
    .achievement-tags {
        justify-content: center;
    }
    
    .achievement-meta {
        justify-content: center;
    }
}

@media (max-width: 768px) {
    .skills {
        padding: 30px 30px !important;
    }
    
    .achievements {
        padding: 30px 30px !important;
    }
    
    .project {
        padding: 25px;
    }
    
    .project-list li {
        font-size: 0.9em;
    }
    
    .project-header h1 {
        font-size: 1.4em;
    }
    
    .hero-image {
        width: 180px;
        height: 180px;
    }
    
    .name {
        font-size: 1.2em;
        white-space: normal;
    }
    
    .contacts-container {
        flex-direction: column;
        gap: 10px;
    }
    
    .logo-container img {
        width: 140px;
        height: 140px;
    }
    
    .achievement-icon {
        width: 70px;
        height: 70px;
    }
    
    .achievement-details h2 {
        font-size: 1.3em;
    }
}
</style>