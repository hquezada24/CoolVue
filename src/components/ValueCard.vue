<!-- ============================================ -->
<!-- COMPONENT 4: ValueCard.vue (child of OurValues) -->
<!-- ============================================ -->

<script setup>
import { defineProps } from 'vue'

defineProps({
  value: {
    type: Object,
    required: true,
  },
})
</script>

<template>
  <div class="value-card">
    <div class="icon">{{ value.icon }}</div>
    <h3>{{ value.title }}</h3>
    <p>{{ value.description }}</p>
  </div>
</template>

<style scoped>
.value-card {
  background: white;
  padding: 2.5rem 2rem;
  border-radius: 20px;
  text-align: center;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.08);
  transition: all 0.3s ease;
}

.value-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.12);
}

.icon {
  font-size: 4rem;
  margin-bottom: 1.5rem;
  line-height: 1;
}

.value-card h3 {
  font-size: 1.5rem;
  color: #2c3e50;
  margin-bottom: 1rem;
  font-weight: 600;
}

.value-card p {
  font-size: 1rem;
  color: #546e7a;
  line-height: 1.6;
}
</style>
