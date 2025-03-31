<script setup>
  import Header from './components/Header.vue';
  import Footer from './components/Footer.vue';
  import HomeContainer from './components/HomeContainer.vue'
import AboutContainer from './components/AboutContainer.vue';
import ServicesContainer from './components/ServicesContainer.vue';
import ContactContainer from './components/ContactContainer.vue';
</script>

<template>
    <Header/>
    <!-- landing page -->
    <HomeContainer/>
    <!-- About Me section -->
     <AboutContainer/>
     <ServicesContainer/>
     <ContactContainer/>

    <Footer/>
</template>