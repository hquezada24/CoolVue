<!-- ============================================ -->
<!-- COMPONENT 3: ProductCard.vue (child of FeaturedProducts) -->
<!-- ============================================ -->

<script setup>
import { RouterLink } from 'vue-router'

defineProps({
  product: {
    type: Object,
    required: true,
  },
})
</script>

<template>
  <div class="product-card">
    <div class="product-icon" :style="{ backgroundColor: product.color }">
      <svg
        v-if="product.type === 'ice-cream'"
        viewBox="0 0 100 100"
        xmlns="http://www.w3.org/2000/svg"
      >
        <circle cx="50" cy="35" r="25" :fill="product.color" opacity="0.8" />
        <path d="M 35 45 L 50 85 L 65 45 Z" fill="#E8A87C" />
      </svg>
      <svg v-else viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
        <rect x="35" y="20" width="30" height="60" rx="15" :fill="product.color" opacity="0.8" />
        <rect x="47" y="15" width="6" height="10" fill="#A0826D" rx="3" />
      </svg>
    </div>
    <h3>{{ product.name }}</h3>
    <p>{{ product.description }}</p>
    <RouterLink to="/menu" class="view-menu-link">View Menu →</RouterLink>
  </div>
</template>

<style scoped>
.product-card {
  background: white;
  border-radius: 20px;
  padding: 2rem;
  text-align: center;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.08);
  transition: all 0.3s ease;
}

.product-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.12);
}

.product-icon {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  margin: 0 auto 1.5rem;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 1rem;
}

.product-icon svg {
  width: 100%;
  height: 100%;
}

.product-card h3 {
  font-size: 1.5rem;
  color: #2c3e50;
  margin-bottom: 0.5rem;
}

.product-card p {
  color: #546e7a;
  font-size: 1rem;
  margin-bottom: 1rem;
  line-height: 1.5;
}

.view-menu-link {
  color: #6ec1e4;
  text-decoration: none;
  font-weight: 600;
  transition: color 0.3s ease;
}

.view-menu-link:hover {
  color: #5ab0d3;
}
</style>
