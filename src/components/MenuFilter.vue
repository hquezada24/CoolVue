<!-- ============================================ -->
<!-- COMPONENT 2: MenuFilter.vue -->
<!-- ============================================ -->

<script setup>
import { defineProps, defineEmits } from 'vue'

defineProps({
  activeFilter: {
    type: String,
    required: true,
  },
})

const emit = defineEmits(['filter-change'])

const filters = [
  { id: 'all', label: 'All Items' },
  { id: 'ice-cream', label: 'Ice Cream' },
  { id: 'ice-pop', label: 'Ice Pops' },
]

const selectFilter = (filterId) => {
  emit('filter-change', filterId)
}
</script>

<template>
  <section class="menu-filter">
    <div class="container">
      <div class="filter-buttons">
        <button
          v-for="filter in filters"
          :key="filter.id"
          :class="['filter-btn', { active: activeFilter === filter.id }]"
          @click="selectFilter(filter.id)"
        >
          {{ filter.label }}
        </button>
      </div>
    </div>
  </section>
</template>

<style scoped>
.menu-filter {
  padding: 2rem;
  background: white;
  border-bottom: 2px solid #f0f0f0;
  position: sticky;
  top: 0;
  z-index: 10;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
}

.filter-buttons {
  display: flex;
  justify-content: center;
  gap: 1rem;
  flex-wrap: wrap;
}

.filter-btn {
  padding: 0.8rem 2rem;
  border: 2px solid #6ec1e4;
  background: white;
  color: #6ec1e4;
  border-radius: 25px;
  font-size: 1rem;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.3s ease;
}

.filter-btn:hover {
  background: #e3f5fb;
  transform: translateY(-2px);
}

.filter-btn.active {
  background: linear-gradient(135deg, #6ec1e4 0%, #89d4f5 100%);
  color: white;
  box-shadow: 0 4px 15px rgba(110, 193, 228, 0.4);
}

@media (max-width: 768px) {
  .menu-filter {
    padding: 1.5rem 1rem;
  }

  .filter-btn {
    padding: 0.7rem 1.5rem;
    font-size: 0.95rem;
  }
}
</style>
