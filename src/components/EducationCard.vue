<template>
  <div class="edu-card">
    <img :src="imgSrc" :alt="title" class="edu-img" />
    <div class="edu-info">
      <h3>{{ title }}</h3>
      <p>{{ description }}</p>
    </div>
  </div>
</template>

<script setup>
defineProps({
  imgSrc: String,
  title: String,
  description: String
})
</script>

<style scoped>
.edu-card {
  display: flex;
  align-items: center;
  background: rgba(255, 255, 255, 0.6);
  backdrop-filter: blur(4px);
  border-radius: 10px;
  padding: 1rem;
  width: 300px;
  max-width: 90%;
  gap: 1rem;
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
  transition: transform 0.3s ease;
}
.edu-card:hover {
  transform: translateY(-5px);
}
.edu-img {
  width: 60px;
  height: 60px;
  object-fit: contain; /* prevent cropping */
  border-radius: 8px; /* or 50% for circle if preferred */
  flex-shrink: 0;
}
.edu-info {
  text-align: left;
}
.edu-info h3 {
  margin: 0;
  font-size: 1rem;
  font-weight: 600;
}
.edu-info p {
  margin: 0.25rem 0 0;
  font-size: 0.85rem;
  color: #555;
}
</style>
