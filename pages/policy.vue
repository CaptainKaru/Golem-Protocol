<script lang="ts"></script>
<template>
    <client-only>
        <NavBar :navAdminMode="'false'"/>
            <div id="gpMain" class="gp-main"></div>
        <Cookies />
    <AboutUs />
        
        <main>
        <h1>PRIVACY POLICY</h1>
        <h2>Living Machine AI MVP</h2>
        <p>Last Updated: [Date]</p>

        <section id="section-1">
            <h2>1. WHO WE ARE</h2>
            <div>
                Living Machine ("we," "us," "our") is an adaptive artificial intelligence platform 
                that learns from interactions to provide personalized, contextual assistance. We are 
                committed to protecting your privacy and handling your personal data transparently 
                in compliance with:

                - General Data Protection Regulation (GDPR) (EU) 2016/679
                - Data Privacy Act of 2012 (Republic Act No. 10173) (Philippines)
                - Implementing Rules and Regulations of the Data Privacy Act

                Data Controller: [Company Name]<br>
                Data Protection Officer (DPO): [Name], [Email Address], [Phone Number]<br>
                Registered Address: [Address]
            </div>
        </section>

        <section id="section-2">
            <h2>2. WHAT PERSONAL DATA WE COLLECT</h2>
            <div>
                <p>Based on the Living Machine MVP use cases, we collect:</p>
                <table border="1" cellpadding="8" cellspacing="0" style="border-collapse: collapse; width: 100%;">
                    <thead>
                        <tr>
                            <th>Category</th>
                            <th>Data Collected</th>
                            <th>Source</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr><td>Identity Data</td><td>Name, username, job title, role</td><td>User registration</td></tr>
                        <tr><td>Contact Data</td><td>Email address, phone number</td><td>User registration</td></tr>
                        <tr><td>Account Data</td><td>Login credentials, account preferences, permissions</td><td>User input</td></tr>
                        <tr><td>Interaction Data</td><td>Conversation history, queries, feedback, session memory, etc.</td><td>AI interactions</td></tr>
                        <tr><td>Usage Data</td><td>Feature usage, task completion rates, interaction patterns</td><td>System monitoring</td></tr>
                        <tr><td>Technical Data</td><td>IP address, device type, browser, OS, log files</td><td>Automated collection</td></tr>
                        <tr><td>Content Data</td><td>Files uploaded, documents processed, emails/calendars</td><td>User input, integrations</td></tr>
                        <tr><td>Professional Data</td><td>Role-specific information for adaptation</td><td>User profile, inference</td></tr>
                        <tr><td>Feedback Data</td><td>Explicit ratings, corrections, satisfaction scores</td><td>User input</td></tr>
                    </tbody>
                </table>
                <p><strong>Special Categories of Data:</strong> We do not intentionally collect sensitive personal data. If you inadvertently provide such data, you consent to its processing as necessary for service provision.</p>
            </div>
        </section>

        <section id="section-3">
            <h2>3. HOW WE USE YOUR PERSONAL DATA (PURPOSES AND LAWFUL BASES)</h2>
            <div>
                <table border="1" cellpadding="8" cellspacing="0" style="border-collapse: collapse; width: 100%;">
                    <thead>
                        <tr>
                            <th>Purpose</th>
                            <th>Data Used</th>
                            <th>Lawful Basis (GDPR)</th>
                            <th>Lawful Basis (DPA 2012)</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr><td>Provide Living Machine Services</td><td>Identity, Contact, Account, Interaction, Content Data</td><td>Contract performance (Art. 6(1)(b))</td><td>Contract fulfillment (Sec. 12(a))</td></tr>
                        <tr><td>Adaptive Learning & Improvement</td><td>Interaction, Usage, Feedback Data</td><td>Legitimate interests (Art. 6(1)(f))</td><td>Legitimate interest (Sec. 12(f))</td></tr>
                        <tr><td>Contextual Awareness (Memory)</td><td>Interaction, Preference Data</td><td>Contract performance</td><td>Contract fulfillment</td></tr>
                        <tr><td>Personalization</td><td>Identity, Role, Interaction Data</td><td>Legitimate interests</td><td>Legitimate interest</td></tr>
                        <tr><td>Autonomous Task Execution</td><td>Content, Integration Data</td><td>Contract performance</td><td>Contract fulfillment</td></tr>
                        <tr><td>Multi-Agent Collaboration</td><td>Task-specific data</td><td>Contract performance</td><td>Contract fulfillment</td></tr>
                        <tr><td>System Monitoring & Security</td><td>Technical, Usage Data</td><td>Legitimate interests / Legal obligation</td><td>Legitimate interest / Legal obligation</td></tr>
                        <tr><td>Confidence Scoring & Self-Monitoring</td><td>Interaction, Feedback Data</td><td>Legitimate interests</td><td>Legitimate interest</td></tr>
                        <tr><td>Customer Support</td><td>Identity, Contact, Interaction Data</td><td>Contract performance / Legitimate interests</td><td>Contract fulfillment / Legitimate interest</td></tr>
                        <tr><td>Compliance with Legal Obligations</td><td>All relevant data</td><td>Legal obligation (Art. 6(1)(c))</td><td>Legal obligation (Sec. 12(c))</td></tr>
                        <tr><td>Marketing Communications</td><td>Contact Data</td><td>Consent (Art. 6(1)(a))</td><td>Consent (Sec. 12(b))</td></tr>
                    </tbody>
                </table>
                <p><strong>Legitimate Interest Assessment:</strong> Our legitimate interests include improving AI performance, understanding user needs, preventing fraud, and ensuring system security. We balance these against your rights and freedoms.</p>
            </div>
        </section>

        <section id="section-4">
            <h2>4. CONSENT AND WITHDRAWAL</h2>
            <div>
                Where processing is based on consent (e.g., marketing, optional features):
                <ul>
                    <li>You may withdraw consent at any time via [settings/preferences link] or by contacting us</li>
                    <li>Withdrawal requests should be directed to the appropriate authority in accordance with applicable laws</li>
                    <li>Withdrawal does not affect the lawfulness of processing before withdrawal</li>
                    <li>Consent for children under 16 requires parental authorization (or under 18 in the Philippines)</li>
                </ul>
            </div>
        </section>

        <section id="section-5">
            <h2>5. AUTOMATED DECISION-MAKING AND PROFILING</h2>
            <div>
                <p>Living Machine uses automated processing, including:</p>
                <table border="1" cellpadding="8" cellspacing="0" style="border-collapse: collapse; width: 100%;">
                    <thead><tr><th>Activity</th><th>Description</th><th>Your Rights</th></tr></thead>
                    <tbody>
                        <tr><td>Confidence Scoring</td><td>AI evaluates confidence in responses and flags low-confidence answers</td><td>You can request human review of critical decisions</td></tr>
                        <tr><td>Personalization</td><td>AI adapts responses based on your role and preferences</td><td>You can opt out of personalization</td></tr>
                        <tr><td>Proactive Assistance</td><td>AI suggests actions based on learned patterns</td><td>You can disable proactive features</td></tr>
                        <tr><td>Task Delegation</td><td>AI routes tasks to specialized sub-agents</td><td>You are informed when sub-agents are used</td></tr>
                    </tbody>
                </table>
                <p>You have the right not to be subject to decisions based solely on automated processing that produce legal or similarly significant effects.</p>
            </div>
        </section>

        <section id="section-6">
            <h2>6. DATA SHARING AND DISCLOSURES</h2>
            <div>
                <p>We share your data only as necessary. We do not sell your personal data to third parties.</p>
            </div>
        </section>

        <section id="section-7">
            <h2>7. INTERNATIONAL DATA TRANSFERS</h2>
            <div>Your personal data may be transferred to and processed in countries outside your country of residence, including the Philippines and the European Economic Area, with appropriate safeguards.</div>
        </section>

        <section id="section-8">
            <h2>8. DATA RETENTION</h2>
            <div>We retain your personal data only as long as necessary for the purposes outlined in this policy, or as required by law.</div>
        </section>

        <section id="section-9">
            <h2>9. YOUR DATA PROTECTION RIGHTS</h2>
            <div>Under GDPR and the Philippine Data Privacy Act, you have rights including access, rectification, erasure, restriction, portability, objection, and withdrawal of consent.</div>
        </section>

        <section id="section-10">
            <h2>10. DATA SECURITY</h2>
            <div>We implement appropriate technical and organizational measures to protect your personal data, including encryption, access controls, and regular security assessments.</div>
        </section>
    </main>
     
    <Cookies />
    <Copyright />
    </client-only>
</template>
<script setup lang="ts">
    import { useSeoMeta, useHead } from '@vueuse/head';
    const title = "Project Golem | Home";
    const description = "Golem Protocol is a responsive artificial intelligence system that adapts to your unique needs, learning from your behaviors and routines to provide seamless assistance across every aspect of your life.";
    useSeoMeta({
        title: () => title,
        description: () => description,
        charset: "utf-8",
        viewport: "width=device-width, initial-scale=1.0"
    });

useHead({
    link: [
    {rel: 'icon', type: 'image/png', href: '/logo.png'},
    {rel: 'stylesheet', href: '/reset.css'},
    {rel: 'stylesheet', href: '/custom.css'} ,
    {rel: 'preconnect', href: 'https://fonts.googleapis.com'},
    {rel: 'preconnect', href: 'https://fonts.gstatic.com', crossorigin: ''},
    {rel: 'stylesheet', href: 'https://fonts.googleapis.com/css2?family=Bitcount:wght@100..900&family=Roboto:ital,wght@0,100..900;1,100..900&display=swap'}
    ]
});
</script>

<style scopeds>
main {
    max-width: 1200px;
    margin: 0 auto;
    padding: 2rem;
    font-family: 'Roboto', sans-serif;
    color: #333;
    line-height: 1.6;
    margin-top: 0px; 
    padding-top: 1rem;  
}

h1 {
    font-size: 2.5rem;
    color: #1a1a2e;
    text-align: center;
    margin-bottom: 0.5rem;
    font-weight: 700;
    letter-spacing: -0.5px;
}

h2 {
    font-size: 1.5rem;
    color: #16213e;
    margin-top: 2rem;
    margin-bottom: 1rem;
    padding-bottom: 0.5rem;
    border-bottom: 2px solid #e94560;
    font-weight: 600;
}

.last-updated {
    text-align: center;
    color: #666;
    font-style: italic;
    margin-bottom: 2rem;
}

section {
    margin-bottom: 2.5rem;
    background: #fff;
    border-radius: 12px;
    padding: 1.5rem;
    box-shadow: 0 2px 8px rgba(0,0,0,0.05);
    transition: transform 0.2s ease, box-shadow 0.2s ease;
}

section:hover {
    box-shadow: 0 4px 16px rgba(0,0,0,0.1);
}

section h2 {
    margin-top: 0;
    border-left: 4px solid #e94560;
    padding-left: 1rem;
}

table {
    width: 100%;
    border-collapse: collapse;
    margin: 1rem 0;
    font-size: 0.9rem;
}

th {
    background: #1a1a2e;
    color: white;
    padding: 12px;
    text-align: left;
    font-weight: 600;
}

td {
    padding: 10px 12px;
    border-bottom: 1px solid #e0e0e0;
    vertical-align: top;
}

tr:hover {
    background: #f5f5f5;
}

.compliance-list {
    list-style: none;
    padding-left: 0;
}

.compliance-list li {
    padding: 0.5rem 0;
    padding-left: 1.5rem;
    position: relative;
}

.compliance-list li:before {
    content: "✓";
    color: #e94560;
    position: absolute;
    left: 0;
    font-weight: bold;
}

.contact-info {
    background: #f8f9fa;
    padding: 1rem;
    border-radius: 8px;
    margin-top: 1rem;
}

.contact-info p {
    margin: 0.5rem 0;
}

.contact-info strong {
    color: #1a1a2e;
}

ul, ol {
    padding-left: 1.5rem;
}

li {
    margin: 0.5rem 0;
}

strong {
    color: #1a1a2e;
}

.table-responsive {
    overflow-x: auto;
}

.special-note {
    background: #fff3cd;
    border-left: 4px solid #ffc107;
    padding: 1rem;
    margin: 1rem 0;
    border-radius: 4px;
}
</style>