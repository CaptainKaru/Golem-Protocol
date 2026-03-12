<script lang="ts"></script>
<template>
    <client-only>
    <NavBar />
    <div id="gpMain" class="gp-main"></div>
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

   const globalDelay = 500;
const allowCookies = useCookie<boolean>("allowCookies", {
 sameSite: "none",
 secure: true,
 maxAge: 60 * 60 * 24,
});
allowCookies.value = allowCookies.value || false;
async function loadModal() {
 const cookieModal = document.getElementById("gpCookieModal") as HTMLDivElement;
 const cookieBox = document.getElementById("gpCookieBox") as HTMLDivElement;
 const cookieX = document.getElementById("gpCookieX") as HTMLDivElement;
 const cookieOK = document.getElementById("gpCookieOK") as HTMLDivElement;
 if ( !cookieModal || !cookieBox || !cookieX || !cookieOK ) return;
 if (allowCookies.value === true) {
 allowAllCookies();
 return;
 }
 showCookiePopup();
 cookieX.addEventListener("click", (e) => {
 showCookiePopup(false);
 });
 cookieOK.addEventListener("click", (e) => {
 allowAllCookies();
 });
}
async function showCookiePopup(show: boolean = true) {
 const cookieBox = document.getElementById("gpCookieBox") as HTMLDivElement;
 const cookieModal = document.getElementById("gpCookieModal") as HTMLDivElement;
 if (!cookieBox || !cookieModal) {
 setTimeout(showCookiePopup, 50);
 return;
 }
 if (!show) {
 cookieBox.classList.add("gp-hidden");
 cookieModal.classList.add("gp-hidden");
 return;
 }

 cookieBox.classList.remove("gp-hidden");
 cookieModal.classList.remove("gp-hidden");
}
let lastCookieClicked = 0;
async function allowAllCookies() {
 if (lastCookieClicked >= Date.now() - globalDelay) return;
 lastCookieClicked = Date.now();
 allowCookies.value = true;
 showCookiePopup(false);
}
onMounted(() => {
 setTimeout(() => {
 loadModal();
 }, 1);
});
</script>

<style scoped></style>
<style>
/* Your scoped styles here */
</style>