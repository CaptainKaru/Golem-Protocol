<template>
    <client-only>
        <header :class="['gp-navbar', navAdminMode]">
            <nav class="gp-nav-left">
                <a href="/" class="gp-nav-home">
                <img src="/logo.png" width=20 height=20 class="gp-nav-logo">
                <span>Golem Protocol</span>
                </a>
            </nav>
            <nav id="gpNavBasic" class="gp-nav-right gp-hidden">
                <ul>
                <li><a href="#" class="gp-nav-link">3R Guide</a></li>
                <li><a href="#" class="gp-nav-link">Leaderboard</a></li>
                <li><a href="#" class="gp-nav-link">Contribute</a></li>
                <li><span id="gpNavBasicLogout" class="gp-nav-link">Logout</span></li>
                </ul>
                </nav>
            <nav id="gpNavAdmin" class="gp-nav-right gp-hidden">
                <ul>
                <li><a href="#" class="gp-nav-link">Settings</a></li>
                <li><a href="#" class="gp-nav-link">Reports</a></li>
                <li><span id="gpNavAdminLogout" class="gp-nav-link">Logout</span></li>
                </ul>
            </nav>
        </header>
    </client-only>
</template>

<script setup lang="ts">
const props = defineProps<{ navAdminMode: string }>();
</script>