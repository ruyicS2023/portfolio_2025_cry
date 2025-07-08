<template>
  <nav class="navbar">
    <div class="navbar-content">
      <div class="logo">Ruyi Cai - Portfolio</div>
      <ul class="nav-links" :class="{ open: showMenu }">
        <li><a href="#home" @click.prevent="navigate('home')">Home</a></li>
        <li><a href="#about" @click.prevent="navigate('about')">About</a></li>
        <li>
          <a href="#projects" @click.prevent="navigate('projects')">Projects</a>
        </li>
        <li>
          <a href="#contact" @click.prevent="navigate('contact')">Contact</a>
        </li>
      </ul>
      <div class="hamburger" @click="showMenu = !showMenu">
        <i :class="showMenu ? 'fas fa-times' : 'fas fa-bars'"></i>
      </div>
    </div>
  </nav>
</template>

<script setup>
import { ref } from "vue";

const showMenu = ref(false);

function navigate(sectionId) {
  const el = document.getElementById(sectionId);
  if (el) el.scrollIntoView({ behavior: "smooth" });
  showMenu.value = false; // Close menu on click
}
</script>

<style scoped>
.navbar {
  position: fixed;
  top: 0;
  width: 100%;
  background: rgba(255, 255, 255, 0.95);
  backdrop-filter: blur(10px);
  display: flex;
  justify-content: center;
  border-bottom: 1px solid #e5e7eb;
  z-index: 50;
}

.navbar-content {
  width: 90%;
  max-width: 960px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0.75rem 1rem;
}

.logo {
  font-weight: 600;
  font-size: 1rem;
}

.nav-links {
  display: flex;
  gap: 1rem;
  list-style: none;
}

.nav-links a {
  text-decoration: none;
  color: #333;
  transition: color 0.3s;
}

.nav-links a:hover {
  color: teal;
}

.hamburger {
  display: none;
  font-size: 1.5rem;
  cursor: pointer;
}

@media (max-width: 768px) {
  .nav-links {
    position: absolute;
    top: 60px;
    right: 0;
    background: white;
    flex-direction: column;
    align-items: flex-start;
    width: 200px;
    padding: 1rem;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    display: none;
  }

  .nav-links.open {
    display: flex;
  }

  .hamburger {
    display: block;
  }
}
</style>
