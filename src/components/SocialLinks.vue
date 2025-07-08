<template>
  <div class="social-links">
    <a href="https://www.linkedin.com/in/ruyi-cai" target="_blank">💼</a>
    <a href="https://github.com/YOUR_GITHUB_USERNAME" target="_blank">🐙</a>
    <a href="mailto:ruyic@alumni.cmu.edu" target="_blank">✉️</a>
  </div>
</template>

<style scoped>
.social-links {
  position: fixed;
  top: 40%;
  left: 1rem;
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
  z-index: 40;
}
a {
  font-size: 1.5rem;
  transition: transform 0.3s;
}
a:hover {
  transform: scale(1.2);
}
</style>
