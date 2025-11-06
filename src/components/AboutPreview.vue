<!-- ============================================ -->
<!-- COMPONENT 4: AboutPreview.vue -->
<!-- ============================================ -->

<script setup>
import { RouterLink } from 'vue-router'
</script>

<template>
  <section class="about-preview">
    <div class="container">
      <div class="content">
        <h2>Crafted with Passion</h2>
        <p>
          Since 2020, we've been creating delicious frozen treats that bring joy to our community.
          Every scoop and every pop is made with premium ingredients and a whole lot of love.
        </p>
        <p>
          From classic flavors to innovative creations, we're dedicated to delivering the perfect
          cool treat for every moment.
        </p>
        <RouterLink to="/about" class="learn-more-btn">Learn More About Us →</RouterLink>
      </div>
      <div class="image-section">
        <div class="decorative-circle"></div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.about-preview {
  background: linear-gradient(135deg, #e0f7fa 0%, #fff5f7 100%);
  padding: 5rem 2rem;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  align-items: center;
  gap: 4rem;
}

.content {
  flex: 1;
}

.content h2 {
  font-size: 3rem;
  color: #2c3e50;
  margin-bottom: 1.5rem;
}

.content p {
  font-size: 1.2rem;
  color: #546e7a;
  line-height: 1.8;
  margin-bottom: 1rem;
}

.learn-more-btn {
  display: inline-block;
  margin-top: 1rem;
  color: #6ec1e4;
  text-decoration: none;
  font-weight: 600;
  font-size: 1.1rem;
  transition: all 0.3s ease;
}

.learn-more-btn:hover {
  color: #5ab0d3;
  transform: translateX(5px);
}

.image-section {
  flex: 1;
  display: flex;
  justify-content: center;
  align-items: center;
}

.decorative-circle {
  width: 300px;
  height: 300px;
  background: linear-gradient(135deg, #ffb7c5 0%, #b4f8c8 50%, #ffd93d 100%);
  border-radius: 50%;
  opacity: 0.3;
  animation: pulse 4s ease-in-out infinite;
}

@keyframes pulse {
  0%,
  100% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.1);
  }
}

@media (max-width: 768px) {
  .container {
    flex-direction: column;
    gap: 2rem;
  }

  .content h2 {
    font-size: 2.2rem;
  }

  .content p {
    font-size: 1.1rem;
  }

  .decorative-circle {
    width: 200px;
    height: 200px;
  }
}
</style>
