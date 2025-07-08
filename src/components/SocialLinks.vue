<template>
  <div class="social-container">
    <button class="social-toggle" @click="toggleLinks">
      <i :class="showLinks ? 'fas fa-times' : 'fas fa-share-alt'"></i>
    </button>
    <Transition name="fade-slide">
      <div v-if="showLinks" class="social-links">
        <a href="https://www.linkedin.com/in/ruyi-cai" target="_blank">
          <i class="fab fa-linkedin"></i>
        </a>
        <a href="https://github.com/ruyicS2023" target="_blank">
          <i class="fab fa-github"></i>
        </a>
        <a href="mailto:ruyic@alumni.cmu.edu" target="_blank">
          <i class="fas fa-envelope"></i>
        </a>
      </div>
    </Transition>
  </div>
</template>

<script setup>
import { ref } from "vue";
const showLinks = ref(false);

function toggleLinks() {
  showLinks.value = !showLinks.value;
}
</script>

<style scoped>
.social-container {
  position: fixed;
  bottom: 2rem;
  left: 1rem;
  display: flex;
  flex-direction: column;
  align-items: center;
  z-index: 50;
}

.social-toggle {
  background: #fff;
  border: none;
  border-radius: 50%;
  width: 3rem;
  height: 3rem;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.15);
  font-size: 1.5rem;
  cursor: pointer;
  transition: transform 0.3s;
}

.social-toggle:hover {
  transform: scale(1.1);
}

.social-links {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
  margin-top: 0.5rem;
}

.social-links a {
  background: #fff;
  border-radius: 50%;
  width: 2.5rem;
  height: 2.5rem;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.15);
  transition: transform 0.3s, background 0.3s;
  text-decoration: none;
}

.social-links a:hover {
  transform: scale(1.1);
  background: #f0f0f0;
}

.fab,
.fas {
  color: #000;
  font-size: 1.25rem;
}
.fade-slide-enter-active,
.fade-slide-leave-active {
  transition: all 0.3s ease;
}

.fade-slide-enter-from,
.fade-slide-leave-to {
  opacity: 0;
  transform: translateY(10px);
}

.fade-slide-enter-to,
.fade-slide-leave-from {
  opacity: 1;
  transform: translateY(0);
}
</style>
