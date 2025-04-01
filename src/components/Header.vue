<script setup>

    import { ref } from 'vue';

    const isDarkMode = ref(false);
    const theme = () => {
        isDarkMode.value = !isDarkMode.value;
        document.body.classList.toggle('dark-mode');
    }

</script>
<template>
    <header>
        <nav class="wrapper">
            <div class="logo">
                <img src="./../assets/logo.png" alt="logo">
            </div>
            <div class="navlinks">
                <a href="#">home</a>
                <a href="#">about</a>
                <a href="#">services</a>
                <a href="#">projects</a>
                <a href="#">contact</a>
                <div class="mode-action">
                    <img v-if="!isDarkMode" src="./../assets/dark.svg"  alt="dark" @click="theme">
                    <img v-else src="./../assets/light.svg" alt="light" @click="theme">
                </div>
            </div>
            <div class="ham-menu">
                <div class="mode-action">
                    <img v-if="!isDarkMode" src="./../assets/dark.svg"  alt="dark" @click="theme">
                    <img v-else src="./../assets/light.svg" alt="light" @click="theme">
                </div>
                <div class="menu">
                    <img src="./../assets/hamMenu.svg" alt="hamMenu">
                </div>
            </div>
        </nav>
    </header>
</template>