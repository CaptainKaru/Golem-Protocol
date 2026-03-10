<script lang="ts"></script>
<template>
    <client-only>
    <NavBar />
    <div id="pgMain" class="pg-main"></div>
    <!-- <Cookies /> -->
    <!-- <Copyright /> -->
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
    {rel: 'stylesheet', href: 'https://fonts.googleapis.com/css2?family=Bitcount+Ink:wght@100..900&display=swap'}
    ]
});
</script>

<style scoped></style>
<style>
/* Your scoped styles here */
</style>