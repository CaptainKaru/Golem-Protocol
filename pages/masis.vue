<script lang="ts"></script>
<template>
    <client-only>
        <NavBar :navAdminMode="'false'"/>

        <main class="personal-page">
            <div class="container">

                <div class="hero-band">
                    <div class="hero-img-wrap">
                        <img src="/masis.png" alt="Monarch Renante G. Asis" class="hero-img" />
                    </div>
                    <div class="hero-text">
                        <h1>Monarch Renante G. Asis</h1>
                        <p class="role">BS Computer Science · Visayas State University · 2024–present</p>
                        <p class="bio">Computer science student. Nothing special — just someone who shows up, writes code, and figures it out along the way. Loves solving problems, and occasionally is the problem.</p>
                    </div>
                </div>

                <div class="body">

                    <div class="card full">
                        <div class="card-label">Contact</div>
                        <div class="contact-row">
                            <div class="icon">
                                <svg viewBox="0 0 24 24"><path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/><polyline points="22,6 12,13 2,6"/></svg>
                            </div>
                            <span class="contact-text"><a href="mailto:24-1-00546@vsu.edu.ph">24-1-00546@vsu.edu.ph</a></span>
                        </div>
                        <div class="contact-row">
                            <div class="icon">
                                <svg viewBox="0 0 24 24"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"/></svg>
                            </div>
                            <span class="contact-text"><a href="https://github.com/mrAsis1" target="_blank">github.com/mrAsis1</a></span>
                        </div>
                        <div class="contact-row">
                            <div class="icon">
                                <svg viewBox="0 0 24 24"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z"/><circle cx="12" cy="10" r="3"/></svg>
                            </div>
                            <span class="contact-text">Maasin City, Southern Leyte, PH</span>
                        </div>
                    </div>

                    <div class="card full">
                        <div class="card-label">Education</div>
                        <div class="item">
                            <div class="dot"></div>
                            <div class="item-body">
                                <div class="item-header">
                                    <span class="item-title">Visayas State University</span>
                                    <span class="item-date">2024 – present</span>
                                </div>
                                <p class="item-sub">Bachelor of Science in Computer Science</p>
                                <p class="item-desc">Baybay City, Leyte · Faculty of Computing</p>
                            </div>
                        </div>
                    </div>

                    <div class="card full">
                        <div class="card-label">Projects</div>
                        <div class="item">
                            <div class="dot"></div>
                            <div class="item-body">
                                <div class="item-header">
                                    <span class="item-title">Student Management System</span>
                                    <span class="item-date">2026</span>
                                </div>
                                <p class="item-desc">Grade management app with full CRUD — add, delete, and edit student records.</p>
                            </div>
                        </div>
                        <div class="item">
                            <div class="dot"></div>
                            <div class="item-body">
                                <div class="item-header">
                                    <span class="item-title">NEXORA</span>
                                    <span class="item-date">2026</span>
                                </div>
                                <p class="item-desc">Built to give athletes and teams the edge through sleek, real-time data insights.</p>
                            </div>
                        </div>
                        <div class="item">
                            <div class="dot"></div>
                            <div class="item-body">
                                <div class="item-header">
                                    <span class="item-title">TravelMate</span>
                                    <span class="item-date">2026</span>
                                </div>
                                <p class="item-desc">Trip planning app for organizing itineraries, packing lists, budgets, and activities.</p>
                            </div>
                        </div>
                    </div>

                    <div class="card full">
                        <div class="card-label">Interests</div>
                        <div class="interests-grid">
                            <div class="interest-item">
                                <div class="icon">
                                    <svg viewBox="0 0 24 24"><circle cx="12" cy="12" r="10"/><path d="M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"/><path d="M2 12h20"/></svg>
                                </div>
                                <div class="interest-text">
                                    <span class="interest-title">Football</span>
                                    <span class="interest-sub">Playing & watching the beautiful game</span>
                                </div>
                            </div>
                        </div>
                    </div>

                    <div class="card full last">
                        <div class="card-label">Skills</div>
                        <div class="skills-grid">
                            <span class="skill-tag hi">C</span>
                            <span class="skill-tag hi">C++</span>
                            <span class="skill-tag hi">Java</span>
                            <span class="skill-tag hi">JavaScript</span>
                            <span class="skill-tag hi">TypeScript</span>
                            <span class="skill-tag">C#</span>
                            <span class="skill-tag">Python</span>
                            <span class="skill-tag">React</span>
                            <span class="skill-tag">HTML</span>
                            <span class="skill-tag">CSS</span>
                            <span class="skill-tag">Assembly</span>
                            <span class="skill-tag">GitHub</span>
                            <span class="skill-tag">SQL</span>
                        </div>
                    </div>

                </div>
            </div>
        </main>

        <Copyright />
    </client-only>
</template>

<script setup lang="ts">
    import { useSeoMeta, useHead } from '@vueuse/head';

    const title = "Monarch Renante G. Asis";
    const description = "The personal page of Monarch Renante G. Asis.";

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
    max-width: 860px;
    padding: 0 24px 24px;
    font-family: "Roboto", Arial, sans-serif;
}

.container {
    background: #ffffff;
    border: 1px solid rgba(15, 23, 42, 0.08);
    border-radius: 20px;
    overflow: hidden;
}

.hero-band {
    background: #0F6E56;
    padding: 40px 40px 0;
    display: flex;
    gap: 32px;
    align-items: flex-end;
}

.hero-img-wrap {
    flex-shrink: 0;
    margin-bottom: -20px;
}

.hero-img {
    width: 110px;
    height: 110px;
    border-radius: 50%;
    border: 4px solid #1D9E75;
    object-fit: cover;
    object-position: center top;
    display: block;
}

.hero-text {
    padding-bottom: 28px;
    flex: 1;
}

.hero-text h1 {
    font-family: "Bitcount", sans-serif;
    font-size: 24px;
    font-weight: 500;
    color: #E1F5EE;
    margin-bottom: 4px;
}

.role {
    font-size: 13px;
    color: #5DCAA5;
    margin-bottom: 10px;
}

.bio {
    font-size: 13px;
    color: #9FE1CB;
    line-height: 1.7;
    max-width: 480px;
}

.body {
    padding: 28px 40px 36px;
    display: flex;
    flex-direction: column;
    gap: 0;
}

.stat-row {
    display: flex;
    gap: 12px;
    margin-bottom: 20px;
    margin-top: 8px;
}

.stat {
    background: #f8fafc;
    border-radius: 10px;
    padding: 14px 24px;
    text-align: center;
    border: 1px solid rgba(15, 23, 42, 0.06);
}

.stat-num {
    font-size: 22px;
    font-weight: 500;
    color: #0F6E56;
}

.stat-lbl {
    font-size: 11px;
    color: #94a3b8;
    margin-top: 2px;
}

.card {
    background: #f8fafc;
    border: 1px solid rgba(15, 23, 42, 0.06);
    border-radius: 14px;
    padding: 20px 22px;
}

.card.full {
    margin-bottom: 16px;
}

.card.last {
    margin-bottom: 0;
}

.card-label {
    font-size: 10px;
    font-weight: 500;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    color: #94a3b8;
    margin-bottom: 14px;
}

.contact-row {
    display: flex;
    align-items: center;
    gap: 10px;
    margin-bottom: 10px;
}

.contact-row:last-child {
    margin-bottom: 0;
}

.icon {
    width: 28px;
    height: 28px;
    border-radius: 8px;
    background: #E1F5EE;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
}

.icon svg {
    width: 14px;
    height: 14px;
    stroke: #0F6E56;
    fill: none;
    stroke-width: 2;
    stroke-linecap: round;
    stroke-linejoin: round;
}

.contact-text {
    font-size: 13px;
    color: #475569;
}

.contact-text a {
    color: #0F6E56;
    text-decoration: none;
}

.item {
    display: flex;
    gap: 14px;
    padding-bottom: 14px;
    margin-bottom: 14px;
    border-bottom: 1px solid #f1f5f9;
}

.item:last-child {
    border-bottom: none;
    margin-bottom: 0;
    padding-bottom: 0;
}

.dot {
    width: 7px;
    height: 7px;
    border-radius: 50%;
    background: #1D9E75;
    margin-top: 6px;
    flex-shrink: 0;
}

.item-body {
    flex: 1;
}

.item-header {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    margin-bottom: 3px;
}

.item-title {
    font-size: 14px;
    font-weight: 500;
    color: #0f172a;
}

.item-date {
    font-size: 11px;
    color: #94a3b8;
    white-space: nowrap;
    margin-left: 8px;
}

.item-sub {
    font-size: 12px;
    color: #64748b;
    margin-bottom: 2px;
}

.item-desc {
    font-size: 12px;
    color: #64748b;
    line-height: 1.6;
}

.interests-grid {
    display: flex;
    flex-direction: column;
    gap: 10px;
}

.interest-item {
    display: flex;
    align-items: center;
    gap: 12px;
}

.interest-text {
    display: flex;
    flex-direction: column;
    gap: 2px;
}

.interest-title {
    font-size: 14px;
    font-weight: 500;
    color: #0f172a;
}

.interest-sub {
    font-size: 12px;
    color: #64748b;
}

.skills-grid {
    display: flex;
    flex-wrap: wrap;
    gap: 7px;
}

.skill-tag {
    font-size: 12px;
    padding: 5px 11px;
    border-radius: 6px;
    background: #ffffff;
    border: 1px solid #e2e8f0;
    color: #334155;
}

.skill-tag.hi {
    background: #E1F5EE;
    border-color: #9FE1CB;
    color: #085041;
}

@media (max-width: 600px) {
    .personal-page {
        margin-top: 90px;
        padding: 0 12px 24px;
    }

    .hero-band {
        flex-direction: column;
        align-items: center;
        text-align: center;
        padding: 28px 24px 0;
    }

    .hero-img-wrap {
        margin-bottom: -16px;
    }

    .bio {
        max-width: 100%;
    }

    .body {
        padding: 20px 20px 28px;
    }

    .stat-row {
        justify-content: center;
    }
}
</style>