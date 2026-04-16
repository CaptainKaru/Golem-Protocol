<script lang="ts"></script>
<template>
    <client-only>
        <NavBar :navAdminMode="'user'"/>
            <div id="gpMain" class="gp-main"></div>
        <Cookies />
        <Copyright /> 
        
        <main>
            <h1>PRIVACY POLICY</h1>
            <h2>Living Machine AI MVP</h2>

            <section id="section-1">
                <h2>WHO WE ARE</h2>
                <div>
                committed to protecting your privacy and handling your personal data transparently 
                in compliance with:

                - General Data Protection Regulation (GDPR) (EU) 2016/679
                - Data Privacy Act of 2012 (Republic Act No. 10173) (Philippines)
                - Implementing Rules and Regulations of the Data Privacy Act

                Data Controller: [Company Name]
                Data Protection Officer (DPO): [Name], [Email Address], [Phone Number]
                Registered Address: [Address]
                </div>
            </section>

            <section id="section-2">

            </section>

            <section id="section-3">
                <div class="category">
                    Identity Data
                    Contact Data
                    Account Data
                    Interaction Data
                    Usage Data 
                </div>

                <div class="data collected">

                </div>

                <div class="source">

                </div>
            </section>
            <section id="section-4"></section>
            <section id="section-5"></section>
            <section id="section-6"></section>
            <section id="section-7"></section>
            <section id="section-8"></section>
            <section id="section-9"></section>
            <section id="section-10"></section>

        </main>
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

<style scoped></style>
<style>
/* Your scoped styles here */
</style>