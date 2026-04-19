<script lang="ts"></script>

<template>
    <client-only>
    <NavBar :navAdminMode="navAdminMode" />
    <div id="gpMain" class="gp-main">
    <span id="gpPageTitle" class="gp-page-title gp-hidden">Latest</span>
    <div id="gpContainer" class="gp-container"></div>
    </div>
    <Cookies />
    <AboutUs />
    <Copyright />
    </client-only>
</template>

<script setup lang="ts">
import { useSeoMeta, useHead } from "@vueuse/head";
import { useRouter } from "vue-router";
import { onMounted, nextTick } from "vue";

const title = "Golem Protocol";
const description = "Golem Protocol is a responsive artificial intelligence system that adapts to your unique needs, learning from your behaviors and routines to provide seamless assistance across every aspect of your life.";

useSeoMeta({
    title: () => title,
    description: () => description,
    charset: "utf-8",
    viewport: "width=device-width, initial-scale=1.0",
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
allowCookies.value = allowCookies.value ?? false;

const retries = useCookie<number>("retries", {
    sameSite: "none",
    secure: true,
    maxAge: 60 * 60,
});
retries.value = retries.value ?? 0;

const username = useCookie<string>("username", {
    sameSite: "none",
    secure: true,
    maxAge: 60 * 60 * 24,
});
username.value = username.value ?? "";

const accessToken = useCookie<string>("accessToken", {
    sameSite: "none",
    secure: true,
    maxAge: 60 * 60 * 24,
});
accessToken.value = accessToken.value ?? "";

const userLevel = useCookie<number>("userLevel", {
    sameSite: "none",
    secure: true,
    maxAge: 60 * 60 * 24,
});
userLevel.value = userLevel.value ?? -1;

const fullName = useCookie<string>("fullName", {
    sameSite: "none",
    secure: true,
    maxAge: 60 * 60 * 24,
});
fullName.value = fullName.value ?? "";

type ContentItem = {
    id: string;
    author: string;
    title: string;
    content: string;
    isSynchronized: number;
    createdAt: number;
};

type ContentResponse = {
    contents: ContentItem[];
};

const router = useRouter();
const gpServer = "https://golem-protocol-api.vercel.app";
let navAdminMode = userLevel.value >= 2 ? "gp-nav-admin" : "";

function getByID<T extends HTMLElement>(id: string) {
    return document.getElementById(id) as T;
}

function showCookiePopup(show = true) {
    const cookieBox = document.getElementById("gpCookieBox");
    const cookieModal = document.getElementById("gpCookieModal");
    
    if (!cookieBox || !cookieModal) return;
    
    if (show) {
        cookieBox.classList.remove("gp-hidden");
        cookieModal.classList.remove("gp-hidden");
    } else {
        cookieBox.classList.add("gp-hidden");
        cookieModal.classList.add("gp-hidden");
    }
}

function allowAllCookies() {
    allowCookies.value = true;
    showCookiePopup(false);
    loadContents(); 
}

function loadModal() {
    setTimeout(() => {
        const cookieModal = document.getElementById("gpCookieModal");
        const cookieBox = document.getElementById("gpCookieBox");
        const cookieX = document.getElementById("gpCookieX");
        const cookieOK = document.getElementById("gpCookieOK");
        
        if (!cookieModal || !cookieBox || !cookieX || !cookieOK) {
            return;
        }
        
        if (allowCookies.value === true) {
            cookieBox.classList.add("gp-hidden");
            cookieModal.classList.add("gp-hidden");
            return;
        }
        
        showCookiePopup();
        
        cookieX.addEventListener("click", () => {
            showCookiePopup(false);
        });
        
        cookieOK.addEventListener("click", () => {
            allowAllCookies();
        });
    }, 100);
}

function checkAuthorizations() {
    if (!accessToken.value) {
        router.push("/login");
        return;
    } else if (userLevel.value >= 2) {
        router.push("/admin");
        return;
    }
    
    const navBasic = getByID<HTMLDivElement>("gpNavBasic");
    const navAdmin = getByID<HTMLDivElement>("gpNavAdmin");
    const navLogout = getByID<HTMLDivElement>("gpNavBasicLogout");
    const pageTitle = getByID<HTMLSpanElement>("gpPageTitle");

    if (!navBasic || !navAdmin || !navLogout || !pageTitle) return;

    navLogout.addEventListener("click", (e) => {
        retries.value = 0;
        username.value = "";
        accessToken.value = "";
        userLevel.value = -1;
        fullName.value = "";
        router.push("/login");
    });

    navAdmin.remove();
    navBasic.classList.remove("gp-hidden");
    pageTitle.classList.remove("gp-hidden");
    
    loadContents();
}

onMounted(() => {
  nextTick(() => {
    loadModal();           
    checkAuthorizations(); 
  });
});

async function loadContents() {
    if (!accessToken.value) return;
    var rawContents = [] as ContentItem[];
    try {
        const query = new URLSearchParams({
            username: username.value,
            userLevel: String(userLevel.value),
            accessToken: accessToken.value,
        }).toString();
        const response = (await $fetch(`${gpServer}/get_contents?${query}`, {
            headers: { "Content-Type": "application/json" },
            method: "GET",
        })) as ContentResponse;
        rawContents = response.contents;
    } catch (e: any) {
        return;
    }
    const container = getByID<HTMLDivElement>("gpContainer");
    if (!container) return;
    container.innerHTML = "";
    const contents = renderContents(rawContents) as HTMLElement;
    container.appendChild(contents);
}

function renderContents(data: ContentItem[]): HTMLElement {
    const parent = document.createElement("div");
    parent.className = "gp-contents";
    data.forEach((item, index) => {
        const wrapper = document.createElement("div");
        wrapper.id = `content-${index}`;
        wrapper.className = "gp-content-box";
        const title = document.createElement("h2");
        title.className = "gp-content-title";
        title.textContent = item.title;
        const meta = document.createElement("p");
        const date = new Date(item.createdAt * 1000);
        const published = date.toLocaleDateString("en-US", {
            year: "numeric",
            month: "long",
            day: "numeric",
        });
        meta.textContent = `by ${item.author} • ${published}`;
        meta.className = "gp-content-meta";
        const content = document.createElement("p");
        content.className = "gp-content-data";
        content.textContent = item.content;
        wrapper.append(title, meta, content);
        parent.appendChild(wrapper);
    });
    return parent;
}
</script>

<style>
.gp-nav-link:hover {
    cursor: pointer;
}
.gp-page-title {
    position: relative;
    margin: 60px auto 0;
    width: 800px;
    max-width: 90%;
    padding: 20px;
    font-size: 1.8em;
    font-weight: bold;
    border-bottom: 1px solid rgba(0, 0, 0, 0.2);
    display: block;
}
.gp-container {
    position: relative;
    margin: 20px auto 0;
    width: 800px;
    max-width: 90%;
}
.gp-content-box {
    margin-bottom: 10px;
    padding: 20px;
    background: #fff;
    border-radius: 3px;
    border: 1px solid rgba(0, 0, 0, 0.2);
    font-family: 'Roboto';
    cursor: pointer;
}
.gp-content-title {
    line-height: 1.5em;
    font-weight: bold;
}
.gp-content-meta {
    font-size: 0.8em;
    color: #666;
}
.gp-content-data {
    margin-top: 10px;
    line-height: 1.5em;
}
</style>