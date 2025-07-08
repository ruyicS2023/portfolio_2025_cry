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
import SocialLinks from "./components/SocialLinks.vue";
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Inter:wght@400;600&display=swap");

body {
  background: url("./assets/bg.jpg") no-repeat center center fixed;
  background-size: cover;
  font-family: "Inter", sans-serif;
  margin: 0;
  color: #333;
  scroll-behavior: smooth;
}
body::before {
  content: "";
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(255, 255, 255, 0.3);
  z-index: -1;
}

@media (max-width: 768px) {
  body {
    background: url("./assets/bg_mobile.jpg") no-repeat center center fixed;
    background-size: cover;
  }
}
</style>
