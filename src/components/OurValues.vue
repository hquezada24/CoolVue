<!-- ============================================ -->
<!-- COMPONENT 3: OurValues.vue -->
<!-- ============================================ -->

<script setup>
import ValueCard from './ValueCard.vue'

const values = [
  {
    id: 1,
    icon: '🌱',
    title: 'Quality Ingredients',
    description:
      'We use only the finest, locally sourced ingredients to create our treats. No artificial flavors or colors.',
  },
  {
    id: 2,
    icon: '❤️',
    title: 'Made with Love',
    description:
      'Every batch is handcrafted with care and attention to detail. We take pride in what we create.',
  },
  {
    id: 3,
    icon: '🌍',
    title: 'Community First',
    description:
      'We support local farmers and businesses, giving back to the community that supports us.',
  },
  {
    id: 4,
    icon: '✨',
    title: 'Innovation',
    description:
      'Constantly experimenting with new flavors and combinations to surprise and delight our customers.',
  },
]
</script>

<template>
  <section class="our-values">
    <div class="container">
      <div class="section-header">
        <h2>What We Stand For</h2>
        <p>Our values guide everything we do</p>
      </div>
      <div class="values-grid">
        <ValueCard v-for="value in values" :key="value.id" :value="value" />
      </div>
    </div>
  </section>
</template>

<style scoped>
.our-values {
  padding: 5rem 2rem;
  background: linear-gradient(135deg, #fff5f7 0%, #e0f7fa 100%);
}

.container {
  max-width: 1200px;
  margin: 0 auto;
}

.section-header {
  text-align: center;
  margin-bottom: 4rem;
}

.section-header h2 {
  font-size: 3rem;
  color: #2c3e50;
  margin-bottom: 1rem;
  font-weight: 700;
}

.section-header p {
  font-size: 1.3rem;
  color: #546e7a;
}

.values-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
}

@media (max-width: 768px) {
  .our-values {
    padding: 3rem 1.5rem;
  }

  .section-header h2 {
    font-size: 2.2rem;
  }

  .section-header p {
    font-size: 1.1rem;
  }

  .values-grid {
    grid-template-columns: 1fr;
  }
}
</style>
