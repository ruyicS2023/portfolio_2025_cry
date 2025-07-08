<template>
  <section id="projects" class="projects-section">
    <h2 class="section-title">Project Experiences</h2>
    <div class="projects-grid">
      <ProjectCard
        imgSrc="/promo.png"
        title="Promo Master"
        description="A centralized platform streamlining promo data and campaign workflows."
      />
      <ProjectCard
        imgSrc="/cluster.svg"
        title="Retail Outlet Clustering"
        description="Developed ML clustering models to segment 30,000+ retail outlets, informing trade strategies."
      />

      <ProjectCard
        imgSrc="/ride.gif"
        title="CampuShare Ride-Sharing App"
        description="Spring Boot microservices app using Kafka for scalable ride matching with optimized scheduling."
      />

      <ProjectCard
        imgSrc="/monitor.gif"
        title="Distributed Monitoring Dashboard"
        description="Real-time system monitoring dashboard using React and REST APIs for queue health and throughput."
      />
    </div>
  </section>
</template>

<script setup>
import ProjectCard from "/src/components/ProjectCard.vue";
</script>

<style scoped>
.projects-section {
  padding: 4rem 1rem;
  text-align: center;
  background: rgba(255, 255, 255, 0.5);
  backdrop-filter: blur(4px);
}
h2 {
  font-size: 2rem;
  font-weight: 600;
  margin-bottom: 2rem;
}
.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 1.5rem;
  margin: 0 auto;
  margin-bottom: 2rem;
  max-width: 80%;
}
</style>
