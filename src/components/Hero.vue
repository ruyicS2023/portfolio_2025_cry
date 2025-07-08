<template>
  <section id="home" class="hero">
    <div class="hero-container">
      <!-- Left: Greetings -->
      <div class="greetings">
        <h1>🌍 Hello</h1>
        <h1>🇨🇳 你好</h1>
        <h1>🇯🇵 こんにちは</h1>
      </div>

      <!-- Divider -->
      <div class="divider"></div>

      <!-- Right: Info -->
      <div class="info">
        <h1>I'm Ruyi Cai</h1>
        <p>Software Engineer focused on ML, Backend, and Impactful Systems.</p>
        <a href="#projects" @click.prevent="scrollTo('projects')" class="cta">
          View Projects
        </a>
      </div>
    </div>
  </section>
</template>



<script setup>
function scrollTo(sectionId) {
  const el = document.getElementById(sectionId);
  if (el) el.scrollIntoView({ behavior: "smooth" });
}
</script>

<style scoped>
h1 {
  font-size: 2.5rem;
  font-weight: 700;
  margin-bottom: 1rem;
}
p {
  font-size: 1.2rem;
  max-width: 600px;
  margin-bottom: 2rem;
}
.hero {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 80vh;
  padding: 2rem 1rem;
  background: rgba(255, 255, 255, 0);
  color: #fff;
}

.hero-container {
  display: flex;
  align-items: center;
  gap: 2rem;
  max-width: 960px;
  width: 100%;
}

.greetings {
  text-align: right;
  font-size: 1.5rem;
  line-height: 2;
  padding: 2rem;
  color: black;
}

.divider {
  height: 300px;
  width: 2px;
  background: #ccc;
}

.info {
  text-align: left;
  max-width: 400px;
  padding: 2rem;
  color: black;
}

.info h1 {
  font-size: 2rem;
  font-weight: 700;
  margin-bottom: 0.5rem;
}

.info p {
  margin-bottom: 4rem;
}

.cta {
  background: teal;
  color: white;
  padding: 1rem;
  border-radius: 5px;
  text-decoration: none;
  font-weight: 500;
  transition: background 0.3s;
}

.cta:hover {
  background: #0d9488;
}

@media (max-width: 768px) {
  .hero-container {
    flex-direction: column;
    text-align: center;
  }
  .divider {
    display: none;
  }
  .greetings {
    text-align: center;
  }
  .info {
    text-align: center;
  }
}

</style>
