<template>
  <nav class="navbar">
    <div class="navbar-content">
      <div class="logo">Ruyi Cai - Portfoliio</div>
      <ul>
        <li><a href="#home" @click.prevent="scrollTo('home')">Home</a></li>
        <li><a href="#about" @click.prevent="scrollTo('about')">About</a></li>
        <li><a href="#projects" @click.prevent="scrollTo('projects')">Project Experiences</a></li>
        <li><a href="#contact" @click.prevent="scrollTo('contact')">Contact</a></li>
      </ul>
    </div>
  </nav>
</template>



<script setup>
function scrollTo(sectionId) {
  const el = document.getElementById(sectionId);
  if (el) el.scrollIntoView({ behavior: "smooth" });
}
</script>

<style scoped>
.navbar {
    position: fixed;
    top: 0;
    width: 100%;
    background: rgba(255, 255, 255, 0.9);
    backdrop-filter: blur(10px);
    display: flex;
    justify-content: center;
    border-bottom: 1px solid #e5e7eb;
    z-index: 50;
}
.navbar-content {
    /* max-width: 960px; */
    width: 90%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0.75rem 1rem;
}
.logo {
  font-weight: 600;
}
ul {
  display: flex;
  gap: 1rem;
  list-style: none;
}
a {
  text-decoration: none;
  color: #333;
  transition: color 0.3s;
}
a:hover {
  color: teal;
}
</style>
