<script setup>
import EducationCard from "/src/components/EducationCard.vue";
</script>

<template>
  <section id="about" class="about-section">
    <h2>About Me</h2>
    <div class="about-container">
      <img src="/src/assets/profile.jpeg" alt="Ruyi Cai" class="profile-pic" />
      <div class="about-text">
        <p>
          Combining software development and data analytics, I'm passionate
          about building systems that deliver real business impact using Python,
          SQL, and modern web frameworks.
        </p>
        <small class="about-footnote">
          *Not actually me in the photo. The penguin just seemed fitting.
        </small>
      </div>
    </div>
    <div class="edu-row">
      <EducationCard
        imgSrc="/cmu.svg"
        title="Carnegie Mellon University"
        description="M.S. Software Engineering, 2023-2024"
      />
      <EducationCard
        imgSrc="/brandeis.png"
        title="Brandeis University"
        description="B.S. Computer Science & International and Global Studies (Double Major), 2018-2022"
      />
    </div>
  </section>
</template>

<style scoped>
.section {
  /* max-width: 600px; */
  margin: 0 auto;
  padding: 4rem 1rem;
  text-align: center;
  background: rgba(255, 255, 255, 0.5);
  backdrop-filter: blur(4px);
}
h2 {
  font-size: 2rem;
  font-weight: 600;
  margin-bottom: 1rem;
}
p {
  font-size: 1rem;
  line-height: 1.6;
}
.about-section {
  padding: 4rem 1rem;
  background: rgba(255, 255, 255, 0.5);
  backdrop-filter: blur(4px);
  text-align: center; /* center the title */
}

.about-section h2 {
  font-size: 2rem;
  font-weight: 700;
  margin-bottom: 2rem;
}

.about-container {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 2rem;
  max-width: 960px;
  margin: 0 auto;
  flex-wrap: wrap;
  margin-bottom: 2rem;
}

.about-footnote {
  display: block;
  margin-top: 1rem;
  font-size: 0.85rem;
  color: #555;
  font-style: italic;
}

.profile-pic {
  width: 180px;
  height: 180px;
  object-fit: cover;
  border-radius: 50%;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  flex-shrink: 0;
}

.about-text {
  max-width: 500px;
  text-align: left; /* left-align text for readability */
}

.about-text p {
  font-size: 1rem;
  line-height: 1.6;
}
.edu-row {
  display: flex;
  gap: 1.5rem;
  justify-content: center;
  align-items: stretch;
  flex-wrap: wrap;
  margin-top: 2rem;
}

@media (max-width: 768px) {
  .about-container {
    flex-direction: column;
    text-align: center;
  }
  .about-text {
    text-align: center;
  }
}
</style>
