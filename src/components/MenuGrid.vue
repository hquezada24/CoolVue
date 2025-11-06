<!-- ============================================ -->
<!-- COMPONENT 3: MenuGrid.vue -->
<!-- ============================================ -->

<script setup>
import { defineProps } from 'vue'
import MenuItem from './MenuItem.vue'

defineProps({
  items: {
    type: Array,
    required: true,
  },
})
</script>

<template>
  <section class="menu-grid">
    <div class="container">
      <div class="grid">
        <MenuItem v-for="item in items" :key="item.id" :item="item" />
      </div>
    </div>
  </section>
</template>

<style scoped>
.menu-grid {
  padding: 3rem 2rem 5rem;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
}

.grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
  gap: 2rem;
}

@media (max-width: 768px) {
  .menu-grid {
    padding: 2rem 1.5rem 3rem;
  }

  .grid {
    grid-template-columns: 1fr;
    gap: 1.5rem;
  }
}
</style>
