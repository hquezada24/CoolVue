<!-- ============================================ -->
<!-- COMPONENT 1: AboutHero.vue -->
<!-- ============================================ -->

<script setup></script>

<template>
  <section class="about-hero">
    <div class="hero-content">
      <h1>Our Story</h1>
      <p class="tagline">Where passion meets frozen perfection</p>
    </div>
    <div class="hero-decoration">
      <div class="circle circle-1"></div>
      <div class="circle circle-2"></div>
      <div class="circle circle-3"></div>
    </div>
  </section>
</template>

<style scoped>
.about-hero {
  background: linear-gradient(135deg, #6ec1e4 0%, #89d4f5 100%);
  padding: 6rem 2rem 4rem;
  text-align: center;
  position: relative;
  overflow: hidden;
}

.hero-content {
  max-width: 800px;
  margin: 0 auto;
  position: relative;
  z-index: 2;
}

.about-hero h1 {
  font-size: 4.5rem;
  color: white;
  margin-bottom: 1rem;
  font-weight: 700;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
}

.tagline {
  font-size: 1.6rem;
  color: rgba(255, 255, 255, 0.95);
  font-weight: 300;
  letter-spacing: 1px;
}

.hero-decoration {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 1;
}

.circle {
  position: absolute;
  border-radius: 50%;
  opacity: 0.1;
}

.circle-1 {
  width: 300px;
  height: 300px;
  background: white;
  top: -100px;
  left: -50px;
}

.circle-2 {
  width: 200px;
  height: 200px;
  background: white;
  bottom: -50px;
  right: 10%;
}

.circle-3 {
  width: 150px;
  height: 150px;
  background: white;
  top: 50%;
  right: -30px;
}

@media (max-width: 768px) {
  .about-hero {
    padding: 4rem 1.5rem 3rem;
  }

  .about-hero h1 {
    font-size: 3rem;
  }

  .tagline {
    font-size: 1.2rem;
  }
}
</style>
