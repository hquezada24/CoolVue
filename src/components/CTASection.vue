<!-- ============================================ -->
<!-- COMPONENT 5: CTASection.vue -->
<!-- ============================================ -->

<script setup>
import { RouterLink } from 'vue-router'
</script>

<template>
  <section class="cta-section">
    <div class="cta-content">
      <h2>Ready to Chill?</h2>
      <p>Explore our full menu of ice creams and ice pops</p>
      <RouterLink to="/menu" class="cta-button">View Full Menu</RouterLink>
    </div>
  </section>
</template>

<style scoped>
.cta-section {
  background: linear-gradient(135deg, #6ec1e4 0%, #89d4f5 100%);
  padding: 5rem 2rem;
  text-align: center;
}

.cta-content h2 {
  font-size: 3rem;
  color: white;
  margin-bottom: 1rem;
}

.cta-content p {
  font-size: 1.3rem;
  color: rgba(255, 255, 255, 0.95);
  margin-bottom: 2rem;
}

.cta-button {
  display: inline-block;
  padding: 1.2rem 3rem;
  background: white;
  color: #6ec1e4;
  text-decoration: none;
  border-radius: 30px;
  font-weight: 700;
  font-size: 1.2rem;
  transition: all 0.3s ease;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.2);
}

.cta-button:hover {
  transform: translateY(-3px);
  box-shadow: 0 6px 20px rgba(0, 0, 0, 0.25);
}

@media (max-width: 768px) {
  .cta-content h2 {
    font-size: 2.2rem;
  }

  .cta-content p {
    font-size: 1.1rem;
  }
}
</style>
