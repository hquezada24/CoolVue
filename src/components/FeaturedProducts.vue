<!-- ============================================ -->
<!-- COMPONENT 2: FeaturedProducts.vue -->
<!-- ============================================ -->

<script setup>
import ProductCard from './ProductCard.vue'

const featuredProducts = [
  {
    id: 1,
    name: 'Strawberry Bliss',
    description: 'Creamy strawberry ice cream made with fresh berries',
    color: '#FFB7C5',
    type: 'ice-cream',
  },
  {
    id: 2,
    name: 'Mint Chocolate Chip',
    description: 'Cool mint with rich chocolate chips',
    color: '#B4F8C8',
    type: 'ice-cream',
  },
  {
    id: 3,
    name: 'Mango Tango Pop',
    description: 'Tropical mango ice pop bursting with flavor',
    color: '#FFD93D',
    type: 'ice-pop',
  },
  {
    id: 4,
    name: 'Berry Blast Pop',
    description: 'Mixed berries frozen to perfection',
    color: '#A28BFE',
    type: 'ice-pop',
  },
]
</script>

<template>
  <section class="featured-products">
    <div class="container">
      <h2>Featured Treats</h2>
      <p class="subtitle">Our customers' favorite flavors</p>
      <div class="products-grid">
        <ProductCard v-for="product in featuredProducts" :key="product.id" :product="product" />
      </div>
    </div>
  </section>
</template>

<style scoped>
.featured-products {
  padding: 5rem 2rem;
  background: white;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
}

.featured-products h2 {
  font-size: 3rem;
  text-align: center;
  color: #2c3e50;
  margin-bottom: 0.5rem;
}

.subtitle {
  text-align: center;
  font-size: 1.2rem;
  color: #546e7a;
  margin-bottom: 3rem;
}

.products-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
}

@media (max-width: 768px) {
  .featured-products {
    padding: 3rem 1.5rem;
  }

  .featured-products h2 {
    font-size: 2.2rem;
  }
}
</style>
