<script setup>

    import { ref } from 'vue';

    const isDarkMode = ref(false);
    
    let ShowModel = ref(false);
 
    const theme = () => {
        isDarkMode.value = !isDarkMode.value;
        document.body.classList.toggle('dark-mode');
    }

    let closeModel = () => {
        ShowModel.value = false;
    }

</script>
<template>
    <header>
        <nav class="wrapper">
            <div class="logo">
                <img src="./../assets/logo.png" alt="logo">
            </div>
            <div class="navlinks">
                <a href="/#home">Home</a>
                <a href="/#about">About</a>
                <a href="/#services">Services</a>
                <a href="/#projects">Projects</a>
                <a href="/#contact">Contact</a>
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
                    <img v-if="!ShowModel" src="./../assets/hamMenu.svg" alt="hamMenu" @click="ShowModel = true">
                    <img v-else src="./../assets/close.svg" alt="close" @click="closeModel">
                </div>
            </div>
        </nav>
        <div class="menulinks" v-if="ShowModel">
            <div class="links">
                <a href="/#home" @click="closeModel">Home</a>
                <a href="/#about" @click="closeModel">About</a>
                <a href="/#services" @click="closeModel">Services</a>
                <a href="/#projects" @click="closeModel">Projects</a>
                <a href="/#contact" @click="closeModel">Contact</a>
            </div>
        </div>
    </header>
</template>