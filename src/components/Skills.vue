<template>
  <section id="skills" class="section">
    <h2 class="section-title">Skills & Tech Stacks</h2>
    <div class="skills-container">
      <div class="skill-category">
        <h3>Programming Languages</h3>
        <div class="skill-badges">
          <span class="badge">Java</span>
          <span class="badge">Python</span>
          <span class="badge">JavaScript</span>
          <span class="badge">HTML/CSS</span>
        </div>
      </div>

      <div class="skill-category">
        <h3>Frameworks & Tools</h3>
        <div class="skill-badges">
          <span class="badge">React</span>
          <span class="badge">Node.js</span>
          <span class="badge">Spring Boot</span>
          <span class="badge">Kafka</span>
          <span class="badge">MS Azure</span>
          <span class="badge">Fabric</span>
          <span class="badge">Docker</span>
          <span class="badge">Git</span>
        </div>
      </div>

      <div class="skill-category">
        <h3>Other</h3>
        <div class="skill-badges">
          <span class="badge">Figma</span>
          <span class="badge">SQL</span>
        </div>
      </div>

      <div class="skill-category">
        <h3>Languages</h3>
        <div class="skill-badges">
          <span class="badge">English (Fluent)</span>
          <span class="badge">Japanese (Fluent, JLPT-N1)</span>
          <span class="badge">Mandarin (Native)</span>
          <span class="badge">Korean (Conversational)</span>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.section {
  padding: 4rem 1rem;
  text-align: center;
  background: rgba(255, 255, 255, 0.5);
  backdrop-filter: blur(4px);
}

.skills-container {
  max-width: 800px;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  gap: 2rem;
}

.skill-category h3 {
  margin-bottom: 0.5rem;
  font-size: 1.2rem;
  font-weight: 600;
}

.skill-badges {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
  justify-content: center;
}

.badge {
  background: #ffffff;
  border: 1px solid #ddd;
  padding: 0.5rem 0.75rem;
  border-radius: 20px;
  font-size: 0.9rem;
  transition: background 0.3s, transform 0.2s;
}

.badge:hover {
  background: teal;
  color: white;
  transform: scale(1.05);
}

.skills-container {
  max-width: 1000px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: 1fr;
  gap: 2rem;
}

@media (min-width: 768px) {
  .skills-container {
    grid-template-columns: 1fr 1fr;
  }
}
</style>
