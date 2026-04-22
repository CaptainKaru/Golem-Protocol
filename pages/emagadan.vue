<script lang="ts"></script>
<template>
    <client-only>
        <NavBar :navAdminMode="'false'"/>

        <main class="personal-page">
            <section class="hero">
                <div class="profile-image">
                    <img src="/emagadan.jpg" alt="Evan Kasimir Magadan" />
                </div>
                <div class="hero-content">
                    <h1>Evan Kasimir Magadan</h1>
                    <p class="email"><a href="mailto:evan.madagan@vsu.edu.ph">evan.madagan@vsu.edu.ph</a></p>
                    <p class="bio">Computer science student. loves solving problems, loves coding, loves collaborating with others</p>
                </div>
            </section>

            <section class="section">
                <h2>Educational Background</h2>
                <div class="education-item">
                    <h3>Visayas State University</h3>
                    <p>Bachelor of Science in Computer Science</p>
                    <p class="dates">2024 – Present</p>
                </div>
            </section>

            <section class="section">
                <h2>Projects</h2>
                <div class="project-item">
                    <h3>neon prism</h3>
                    <p class="dates">2026</p>
                    <p>Color picker like a website for artist to mix and get colors</p>
                </div>
            </section>

            <section class="section">
                <h2>Skills</h2>
                <ul>
                    <li>C</li>
                    <li>C++</li>
                    <li>C#</li>
                    <li>Java</li>
                    <li>React</li>
                    <li>HTML</li>
                    <li>CSS</li>
                    <li>Assembly</li>
                    <li>GitHub</li>
                    <li>JavaScript</li>
                    <li>TypeScript</li>
                    <li>SQL</li>
                </ul>
            </section>
        </main>

        <Cookies />
        <Copyright />
    </client-only>
</template>

<script setup lang="ts">
    import { useSeoMeta, useHead } from '@vueuse/head';

    const title = "Evan Kasimir Magadan";
    const description = "The personal page of Evan Kasimir Magadan.";

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
            { rel: 'stylesheet', href: 'https://fonts.googleapis.com/css2?family=Bitcount:wght@100..900&family=Roboto:ital,wght@0,100..900;1,100..900&display=swap' }
        ]
    });
</script>

<style scoped>
.personal-page {
    margin: 80px auto 40px;
    max-width: 800px;
    padding: 0 24px 24px;
    color: #1f2937;
}

.hero {
    display: flex;
    align-items: center;
    gap: 24px;
    margin-bottom: 40px;
    padding: 32px;
    background: #ffffff;
    border-radius: 22px;
    border: 1px solid rgba(15, 23, 42, 0.08);
    box-shadow: 0 24px 50px rgba(15, 23, 42, 0.06);
}

.profile-image {
    display: flex;
    justify-content: center;
    align-items: center;
}

.profile-image img {
    width: 120px;
    height: 120px;
    border-radius: 50%;
    object-fit: cover;
    object-position: center 30%; 
    border: 4px solid #f2f4f7;
    display: block;
}

.hero-content h1 {
    margin: 0 0 8px;
    font-size: 2.5rem;
    color: #0f172a;
}

.email {
    color: #475569;
    font-size: 1.1rem;
    margin: 8px 0;
}

.bio {
    color: #334155;
    font-size: 1.1rem;
    line-height: 1.6;
}

.section {
    margin-bottom: 40px;
    padding: 24px;
    background: #ffffff;
    border-radius: 22px;
    border: 1px solid rgba(15, 23, 42, 0.08);
    box-shadow: 0 18px 40px rgba(15, 23, 42, 0.05);
    transition: all 0.3s ease;
}

.section:hover {
    transform: translateY(-5px);
    box-shadow: 0 25px 60px rgba(15, 23, 42, 0.15);
    border-color: rgba(25, 118, 210, 0.2);
}

.section h2 {
    margin: 0 0 20px;
    color: #0f172a;
    font-size: 1.5rem;
    border-bottom: 2px solid #e2e8f0;
    padding-bottom: 8px;
}

.experience-item h3,
.education-item h3,
.project-item h3 {
    margin: 0 0 8px;
    color: #0f172a;
    font-size: 1.2rem;
}

.dates {
    color: #64748b;
    font-size: 0.9rem;
    margin: 4px 0;
}

.section p {
    color: #334155;
    line-height: 1.6;
    margin: 8px 0;
}

.section ul {
    list-style: none;
    padding: 0;
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
}

.section ul li {
    background: #f1f5f9;
    padding: 8px 16px;
    border-radius: 20px;
    font-size: 0.95rem;
    color: #334155;
}

@media (max-width: 768px) {
    .hero {
        flex-direction: column;
        text-align: center;
    }

    .personal-page {
        margin-top: 90px;
        padding: 0 18px 18px;
    }

    .hero,
    .section {
        padding: 20px;
    }
}
</style>