<!-- ============================================ -->
<!-- COMPONENT 1: MenuHeader.vue -->
<!-- ============================================ -->

<script setup></script>

<template>
  <section class="menu-header">
    <div class="container">
      <h1>Our Menu</h1>
      <p>Handcrafted frozen treats made fresh daily with premium ingredients</p>
    </div>
  </section>
</template>

<style scoped>
.menu-header {
  padding: 4rem 2rem 3rem;
  text-align: center;
  background: linear-gradient(135deg, #e0f7fa 0%, #fff5f7 100%);
}

.container {
  max-width: 800px;
  margin: 0 auto;
}

.menu-header h1 {
  font-size: 4rem;
  color: #2c3e50;
  margin-bottom: 1rem;
  font-weight: 700;
}

.menu-header p {
  font-size: 1.3rem;
  color: #546e7a;
  line-height: 1.6;
}

@media (max-width: 768px) {
  .menu-header {
    padding: 3rem 1.5rem 2rem;
  }

  .menu-header h1 {
    font-size: 2.5rem;
  }

  .menu-header p {
    font-size: 1.1rem;
  }
}
</style>
