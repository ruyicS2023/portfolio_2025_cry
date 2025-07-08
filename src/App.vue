<template>
  <div id="app">
    <Navbar />
    <Hero />
    <SocialLinks />
    <About />
    <Projects />
    <Contact />
  </div>
</template>

<script setup>
import Navbar from "./components/Navbar.vue";
import Hero from "./components/Hero.vue";
import About from "./components/About.vue";
import Projects from "./components/Projects.vue";
import Contact from "./components/Contact.vue";
// import SocialLinks from "./components/SocialLinks.vue";
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Inter:wght@400;600&display=swap");

body {
    background: url('./assets/bg.jpg') no-repeat center center fixed;
    background-size: cover;
    font-family: "Inter", sans-serif;
    margin: 0;
    color: #333;
    scroll-behavior: smooth;
}


/* .container {
  width: 100vw;
  min-height: 100vh;
  margin: 0;
  padding: 0;
} */
</style>
