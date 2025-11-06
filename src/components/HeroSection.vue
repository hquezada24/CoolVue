<!-- ============================================ -->
<!-- COMPONENT 1: HeroSection.vue -->
<!-- ============================================ -->

<script setup>
import { RouterLink } from 'vue-router'
</script>

<template>
  <section class="hero">
    <div class="hero-content">
      <h2>Cool Treats for Hot Days</h2>
      <p>Handcrafted ice cream & refreshing ice pops made with love and the finest ingredients</p>
      <div class="hero-buttons">
        <RouterLink to="/menu" class="btn btn-primary">View Menu</RouterLink>
        <RouterLink to="/about" class="btn btn-secondary">Our Story</RouterLink>
      </div>
    </div>
    <div class="hero-image">
      <div class="ice-cream-illustration">
        <svg viewBox="0 0 200 300" xmlns="http://www.w3.org/2000/svg">
          <defs>
            <linearGradient id="strawberry" x1="0%" y1="0%" x2="0%" y2="100%">
              <stop offset="0%" style="stop-color: #ffb7c5; stop-opacity: 1" />
              <stop offset="100%" style="stop-color: #ff8fa3; stop-opacity: 1" />
            </linearGradient>
            <linearGradient id="mint" x1="0%" y1="0%" x2="0%" y2="100%">
              <stop offset="0%" style="stop-color: #b4f8c8; stop-opacity: 1" />
              <stop offset="100%" style="stop-color: #a0e7b8; stop-opacity: 1" />
            </linearGradient>
            <linearGradient id="vanilla" x1="0%" y1="0%" x2="0%" y2="100%">
              <stop offset="0%" style="stop-color: #fff5e1; stop-opacity: 1" />
              <stop offset="100%" style="stop-color: #ffe4b5; stop-opacity: 1" />
            </linearGradient>
          </defs>

          <circle cx="100" cy="80" r="45" fill="url(#strawberry)" />
          <circle cx="100" cy="130" r="45" fill="url(#mint)" />
          <circle cx="100" cy="180" r="45" fill="url(#vanilla)" />

          <path d="M 65 200 L 100 280 L 135 200 Z" fill="#E8A87C" />
          <line x1="75" y1="210" x2="85" y2="240" stroke="#D4956A" stroke-width="3" />
          <line x1="100" y1="210" x2="100" y2="260" stroke="#D4956A" stroke-width="3" />
          <line x1="125" y1="210" x2="115" y2="240" stroke="#D4956A" stroke-width="3" />
          <path d="M 70 215 Q 100 220 130 215" stroke="#D4956A" stroke-width="2" fill="none" />
          <path d="M 75 230 Q 100 235 125 230" stroke="#D4956A" stroke-width="2" fill="none" />
          <path d="M 80 245 Q 100 250 120 245" stroke="#D4956A" stroke-width="2" fill="none" />

          <circle cx="85" cy="75" r="3" fill="rgba(255,255,255,0.6)" />
          <circle cx="110" cy="125" r="3" fill="rgba(255,255,255,0.6)" />
          <circle cx="90" cy="175" r="3" fill="rgba(255,255,255,0.6)" />
        </svg>
      </div>
    </div>
  </section>
</template>

<style scoped>
.hero {
  background: linear-gradient(135deg, #fff5f7 0%, #e0f7fa 100%);
  padding: 4rem 2rem;
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 4rem;
  min-height: 500px;
}

.hero-content {
  max-width: 500px;
}

.hero-content h2 {
  font-size: 3.5rem;
  font-weight: 700;
  color: #2c3e50;
  margin-bottom: 1rem;
  line-height: 1.2;
}

.hero-content p {
  font-size: 1.3rem;
  color: #546e7a;
  margin-bottom: 2rem;
  line-height: 1.6;
}

.hero-buttons {
  display: flex;
  gap: 1rem;
}

.btn {
  padding: 1rem 2rem;
  border-radius: 30px;
  text-decoration: none;
  font-weight: 600;
  font-size: 1.1rem;
  transition: all 0.3s ease;
  display: inline-block;
}

.btn-primary {
  background: linear-gradient(135deg, #6ec1e4 0%, #89d4f5 100%);
  color: white;
  box-shadow: 0 4px 15px rgba(110, 193, 228, 0.4);
}

.btn-primary:hover {
  transform: translateY(-3px);
  box-shadow: 0 6px 20px rgba(110, 193, 228, 0.5);
}

.btn-secondary {
  background: white;
  color: #6ec1e4;
  border: 2px solid #6ec1e4;
}

.btn-secondary:hover {
  background: #6ec1e4;
  color: white;
  transform: translateY(-3px);
}

.hero-image {
  flex-shrink: 0;
}

.ice-cream-illustration {
  width: 250px;
  height: 350px;
  animation: float 3s ease-in-out infinite;
}

@keyframes float {
  0%,
  100% {
    transform: translateY(0px);
  }
  50% {
    transform: translateY(-20px);
  }
}

@media (max-width: 768px) {
  .hero {
    flex-direction: column;
    padding: 3rem 1.5rem;
    gap: 2rem;
  }

  .hero-content h2 {
    font-size: 2.5rem;
  }

  .hero-content p {
    font-size: 1.1rem;
  }

  .hero-buttons {
    flex-direction: column;
  }

  .ice-cream-illustration {
    width: 200px;
    height: 300px;
  }
}
</style>
