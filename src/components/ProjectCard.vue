<template>
    <div class="project-card">
      <img :src="imgSrc" :alt="title" class="project-img" />
      <div class="project-info">
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
  .project-card {
    background: rgba(255, 255, 255, 0.7);
    backdrop-filter: blur(3px);
    border-radius: 12px;
    overflow: hidden;
    box-shadow: 0 4px 12px rgba(0,0,0,0.1);
    transition: transform 0.3s ease;
    cursor: pointer;
  }
  .project-card:hover {
    transform: translateY(-5px);
  }
  .project-img {
    width: 100%;
    aspect-ratio: 1 / 1;
    object-fit: cover;
    border-bottom: 1px solid #ddd;
  }

  .project-info {
    padding: 1rem;
    text-align: left;
  }
  .project-info h3 {
    margin: 0 0 0.5rem;
    font-size: 1.1rem;
    font-weight: 600;
  }
  .project-info p {
    margin: 0;
    font-size: 0.9rem;
    color: #555;
  }
  </style>