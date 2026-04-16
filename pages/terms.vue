<script lang="ts"></script>
<template>
    <client-only>
        <!-- Design reviewed with regulatory compliance co-developers for clarity, accessibility, and corporate minimalism -->
        <NavBar :navAdminMode="'false'"/>

        <main class="terms-page">
            <section class="terms-hero">
                <div>
                    <p class="eyebrow">Terms of Service</p>
                    <h1>Living Machine AI MVP</h1>
                    <p class="subtitle">Last updated: April 16, 2026</p>
                </div>
            </section>

            <section class="terms-content">
                <article>
                    <h2>1. Introduction and Scope</h2>
                    <p>These Terms of Service ("Terms") govern your access to and use of the Living Machine AI system ("Living Machine," "we," "our," or "us"), an adaptive artificial intelligence platform. By accessing or using Living Machine, you enter into a legally binding agreement with us.</p>
                    <h3>Key Features Covered</h3>
                    <ul>
                        <li>Adaptive learning and contextual awareness</li>
                        <li>Autonomous task execution and personalization</li>
                        <li>Self-monitoring and multi-agent collaboration</li>
                        <li>Multi-modal interaction capabilities</li>
                    </ul>

                    <h2>2. Eligibility and Account Registration</h2>
                    <p>You must be at least 18 years old to use Living Machine. By registering, you represent that you have the legal capacity to enter these Terms. You are responsible for maintaining the confidentiality of your account credentials and all activities under your account.</p>

                    <h2>3. Data Protection and Privacy</h2>
                    <p>We process your personal data in accordance with our <a href="/policy">Privacy Policy</a> and in compliance with:</p>
                    <ul>
                        <li>The General Data Protection Regulation (GDPR) (EU)</li>
                        <li>The Data Privacy Act of 2012 (Republic Act No. 10173) (Philippines)</li>
                    </ul>

                    <h3>3.1 Lawful Bases for Processing</h3>
                    <p>We process your personal data only when we have a lawful basis, including:</p>
                    <ul>
                        <li>Performance of a contract (providing the Living Machine services)</li>
                        <li>Your consent (for optional features like marketing)</li>
                        <li>Compliance with legal obligations</li>
                        <li>Our legitimate interests (improving the AI system, fraud prevention), balanced against your rights and freedoms</li>
                    </ul>

                    <h3>3.2 Types of Data Processed</h3>
                    <p>We collect and process:</p>
                    <ul>
                        <li><strong>Account Information:</strong> Name, email address, contact details</li>
                        <li><strong>Usage Data:</strong> Interactions with the AI, conversation history, preferences</li>
                        <li><strong>Technical Data:</strong> Device information, IP address, log data</li>
                        <li><strong>Content:</strong> Files, messages, and other materials you submit to the system</li>
                        <li><strong>Sensitive data:</strong> Processed only with your explicit consent or as permitted by law</li>
                    </ul>

                    <h2>4. Your Data Protection Rights</h2>
                    <p>Under GDPR and the Philippine Data Privacy Act, you have the following rights:</p>
                    <table class="terms-table">
                        <thead>
                            <tr>
                                <th>Right</th>
                                <th>Description</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr>
                                <td>Right to Access</td>
                                <td>Request confirmation of whether we process your data and access to that data</td>
                            </tr>
                            <tr>
                                <td>Right to Rectification</td>
                                <td>Request correction of inaccurate or incomplete data</td>
                            </tr>
                            <tr>
                                <td>Right to Erasure</td>
                                <td>Request deletion of your data where there is no compelling reason for continued processing</td>
                            </tr>
                            <tr>
                                <td>Right to Restriction</td>
                                <td>Request restriction of processing in certain circumstances</td>
                            </tr>
                            <tr>
                                <td>Right to Data Portability</td>
                                <td>Receive your data in a structured, commonly used format and transmit it to another controller</td>
                            </tr>
                            <tr>
                                <td>Right to Object</td>
                                <td>Object to processing based on legitimate interests or for direct marketing</td>
                            </tr>
                            <tr>
                                <td>Right to Withdraw Consent</td>
                                <td>Withdraw consent at any time (withdrawal does not affect lawfulness of prior processing)</td>
                            </tr>
                            <tr>
                                <td>Right to Lodge a Complaint</td>
                                <td>File a complaint with a supervisory authority (NPC in the Philippines or relevant EU authority)</td>
                            </tr>
                        </tbody>
                    </table>
                    <p>To exercise these rights, contact our Data Protection Officer at <a href="mailto:dpo@golemprotocol.com">dpo@golemprotocol.com</a>. We will respond within one month as required by law.</p>

                    <h2>5. Data Retention</h2>
                    <p>We retain your personal data only as long as necessary to fulfill the purposes for which it was collected, including:</p>
                    <ul>
                        <li>Providing the Living Machine services</li>
                        <li>Complying with legal obligations</li>
                        <li>Resolving disputes</li>
                        <li>Enforcing our agreements</li>
                    </ul>
                    <p>Specific retention periods are documented in our Data Retention Policy. Upon termination of your account, we will delete or anonymize your data unless retention is required by law.</p>

                    <h2>6. Data Security</h2>
                    <p>We implement appropriate technical and organizational measures to protect your personal data against unauthorized or unlawful processing and against accidental loss, destruction, or damage, including:</p>
                    <ul>
                        <li>Encryption of data in transit and at rest</li>
                        <li>Access controls and authentication measures</li>
                        <li>Regular security assessments</li>
                        <li>Breach notification procedures</li>
                    </ul>
                    <p>In the event of a data breach affecting your personal data, we will notify you and relevant supervisory authorities as required by law.</p>

                    <h2>7. International Data Transfers</h2>
                    <p>Your personal data may be transferred to and processed in countries outside your country of residence, including the Philippines and the European Economic Area. We ensure such transfers comply with applicable data protection laws through:</p>
                    <ul>
                        <li>Adequacy decisions</li>
                        <li>Standard Contractual Clauses</li>
                        <li>Binding Corporate Rules</li>
                        <li>Other lawful transfer mechanisms</li>
                    </ul>

                    <h2>8. AI Learning and Improvement</h2>
                    <p>Living Machine learns from user interactions to improve its performance. By using the service, you acknowledge that:</p>
                    <ul>
                        <li>Your interactions may be used to train and improve the AI system</li>
                        <li>We employ anonymization and aggregation techniques where possible</li>
                        <li>You may opt out of having your data used for training by contacting us (opt-out may limit certain features)</li>
                    </ul>

                    <h2>9. User Responsibilities</h2>
                    <p>You agree not to:</p>
                    <ul>
                        <li>Use Living Machine for illegal purposes or to violate any laws</li>
                        <li>Infringe on intellectual property rights</li>
                        <li>Upload malicious code or attempt to compromise system security</li>
                        <li>Reverse engineer or extract the underlying AI models</li>
                        <li>Provide false or misleading information</li>
                        <li>Use the service to process special categories of data without proper legal basis</li>
                    </ul>

                    <h2>10. Third-Party Services and Integrations</h2>
                    <p>Living Machine may integrate with third-party services (calendars, email, databases). When you enable such integrations, your data will be processed according to the third party's terms and privacy policies. We are not responsible for third-party practices.</p>

                    <h2>11. Changes to These Terms</h2>
                    <p>We may update these Terms from time to time. We will notify you of material changes via email or through the service. Continued use after changes constitutes acceptance of the revised Terms.</p>

                    <h2>12. Contact Information</h2>
                    <div class="contact-grid">
                        <div>
                            <p class="label">Data Protection Officer</p>
                            <p>Rodney M. Maniego Jr.</p>
                            <p><a href="mailto:dpo@golemprotocol.com">dpo@golemprotocol.com</a></p>
                            <p>+63 917 123 4567</p>
                        </div>
                        <div>
                            <p class="label">National Privacy Commission (Philippines)</p>
                            <p><a href="https://privacy.gov.ph" target="_blank" rel="noreferrer">privacy.gov.ph</a></p>
                        </div>
                        <div>
                            <p class="label">Relevant EU Supervisory Authority</p>
                            <p>As applicable based on your location</p>
                        </div>
                    </div>

                    <div class="terms-note">
                        <p><strong>Compliance note:</strong> Lawful bases, data subject rights, and sensitive data handling are documented to align with GDPR and Philippine data protection requirements.</p>
                    </div>
                </article>
            </section>
        </main>

        <Cookies />
        <Copyright />
    </client-only>
</template>

<script setup lang="ts">
    import { useSeoMeta, useHead } from '@vueuse/head';

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
            { rel: 'stylesheet', href: 'https://fonts.googleapis.com/css2?family=Bitcount:wght@100..900&family=Roboto:ital,wght@0,100..900;1,100..900&display=swap' }
        ]
    });
</script>

<style scoped>
.terms-page {
    margin: 80px auto 40px;
    max-width: 980px;
    padding: 0 24px 24px;
    color: #1f2937;
}

.terms-hero {
    margin-bottom: 32px;
    padding: 32px 28px;
    background: #ffffff;
    border: 1px solid rgba(15, 23, 42, 0.08);
    border-radius: 22px;
    box-shadow: 0 24px 50px rgba(15, 23, 42, 0.06);
}

.eyebrow {
    margin: 0 0 12px;
    color: #475569;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    font-size: 0.8rem;
}

h1 {
    margin: 0;
    font-size: clamp(2.1rem, 1.9rem + 0.8vw, 3rem);
    line-height: 1.05;
    color: #0f172a;
}

.subtitle {
    margin: 12px 0 0;
    color: #475569;
    font-size: 0.95rem;
}

.terms-content {
    background: #ffffff;
    border-radius: 22px;
    border: 1px solid rgba(15, 23, 42, 0.08);
    padding: 32px 32px 28px;
    box-shadow: 0 18px 40px rgba(15, 23, 42, 0.05);
}

.terms-content h2,
.terms-content h3 {
    color: #0f172a;
    margin-top: 36px;
}

.terms-content h2 {
    font-size: 1.35rem;
}

.terms-content h3 {
    font-size: 1.05rem;
}

.terms-content p,
.terms-content li,
.terms-content .label {
    color: #334155;
    line-height: 1.8;
    font-size: 1rem;
}

.terms-content ul {
    margin: 16px 0 0 1.2rem;
    padding-left: 0;
}

.terms-content ul li {
    margin: 10px 0;
}

.terms-table {
    width: 100%;
    border-collapse: collapse;
    margin: 18px 0;
    font-size: 0.98rem;
}

.terms-table th,
.terms-table td {
    padding: 14px 16px;
    border: 1px solid rgba(148, 163, 184, 0.25);
    text-align: left;
    vertical-align: top;
}

.terms-table th {
    background: #f8fafc;
    color: #0f172a;
    font-weight: 700;
}

.contact-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
    gap: 18px;
    margin-top: 18px;
}

.contact-grid .label {
    font-weight: 700;
    color: #0f172a;
    margin-bottom: 6px;
}

.terms-note {
    margin-top: 28px;
    padding: 22px;
    background: #f8fafc;
    border-left: 4px solid #2563eb;
    border-radius: 14px;
}

.terms-note p {
    margin: 0;
}

a {
    color: #2563eb;
    text-decoration: none;
}

a:hover {
    text-decoration: underline;
}

@media (max-width: 768px) {
    .terms-page {
        margin-top: 90px;
        padding: 0 18px 18px;
    }

    .terms-hero,
    .terms-content {
        padding: 24px;
    }
}
</style>