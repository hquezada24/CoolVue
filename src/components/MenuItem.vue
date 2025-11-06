<!-- ============================================ -->
<!-- COMPONENT 4: MenuItem.vue (child of MenuGrid) -->
<!-- ============================================ -->

<script setup>
import { defineProps } from 'vue'

defineProps({
  item: {
    type: Object,
    required: true,
  },
})
</script>

<template>
  <div class="menu-item">
    <div class="item-badge" v-if="item.popular">
      <span>⭐ Popular</span>
    </div>
    <div class="item-icon" :style="{ backgroundColor: item.color }">
      <svg
        v-if="item.category === 'ice-cream'"
        viewBox="0 0 100 100"
        xmlns="http://www.w3.org/2000/svg"
      >
        <circle cx="50" cy="35" r="25" :fill="item.color" opacity="0.9" />
        <circle cx="50" cy="30" r="20" :fill="item.color" opacity="0.7" />
        <path d="M 35 45 L 50 85 L 65 45 Z" fill="#E8A87C" />
        <line x1="40" y1="50" x2="45" y2="65" stroke="#D4956A" stroke-width="2" />
        <line x1="50" y1="50" x2="50" y2="75" stroke="#D4956A" stroke-width="2" />
        <line x1="60" y1="50" x2="55" y2="65" stroke="#D4956A" stroke-width="2" />
      </svg>
      <svg v-else viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg">
        <rect x="35" y="25" width="30" height="55" rx="15" :fill="item.color" opacity="0.9" />
        <rect x="47" y="20" width="6" height="10" fill="#A0826D" rx="3" />
        <ellipse cx="50" cy="28" rx="15" ry="8" :fill="item.color" opacity="0.7" />
      </svg>
    </div>
    <div class="item-content">
      <h3>{{ item.name }}</h3>
      <p>{{ item.description }}</p>
      <div class="item-footer">
        <span class="price">{{ item.price }}</span>
        <span class="category-tag">{{
          item.category === 'ice-cream' ? '🍦 Ice Cream' : '🍡 Ice Pop'
        }}</span>
      </div>
    </div>
  </div>
</template>

<style scoped>
.menu-item {
  background: white;
  border-radius: 20px;
  padding: 2rem;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.08);
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
}

.menu-item:hover {
  transform: translateY(-8px);
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.15);
}

.item-badge {
  position: absolute;
  top: 1rem;
  right: 1rem;
  background: linear-gradient(135deg, #ffd93d 0%, #ffc107 100%);
  color: white;
  padding: 0.4rem 1rem;
  border-radius: 20px;
  font-size: 0.85rem;
  font-weight: 600;
  box-shadow: 0 2px 8px rgba(255, 193, 7, 0.3);
}

.item-icon {
  width: 120px;
  height: 120px;
  border-radius: 50%;
  margin: 0 auto 1.5rem;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 1.5rem;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
}

.item-icon svg {
  width: 100%;
  height: 100%;
}

.item-content {
  text-align: center;
}

.item-content h3 {
  font-size: 1.6rem;
  color: #2c3e50;
  margin-bottom: 0.8rem;
  font-weight: 600;
}

.item-content p {
  color: #546e7a;
  font-size: 1rem;
  line-height: 1.6;
  margin-bottom: 1.5rem;
  min-height: 3rem;
}

.item-footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-top: 1rem;
  border-top: 2px solid #f0f0f0;
}

.price {
  font-size: 1.5rem;
  font-weight: 700;
  color: #6ec1e4;
}

.category-tag {
  font-size: 0.9rem;
  color: #546e7a;
  background: #f5f5f5;
  padding: 0.4rem 0.8rem;
  border-radius: 15px;
}
</style>
