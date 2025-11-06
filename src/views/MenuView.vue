<!-- MENU PAGE (views/MenuView.vue) -->
<script setup>
import { ref } from 'vue'
import MenuHeader from '@/components/MenuHeader.vue'
import MenuFilter from '@/components/MenuFilter.vue'
import MenuGrid from '@/components/MenuGrid.vue'

const activeFilter = ref('all')

const menuItems = [
  // Ice Creams
  {
    id: 1,
    name: 'Strawberry Bliss',
    description: 'Fresh strawberries blended into creamy perfection',
    price: '$4.99',
    category: 'ice-cream',
    color: '#FFB7C5',
    popular: true,
  },
  {
    id: 2,
    name: 'Mint Chocolate Chip',
    description: 'Cool mint with premium dark chocolate chips',
    price: '$4.99',
    category: 'ice-cream',
    color: '#B4F8C8',
    popular: true,
  },
  {
    id: 3,
    name: 'Vanilla Bean Dream',
    description: 'Classic Madagascar vanilla with real bean specks',
    price: '$4.49',
    category: 'ice-cream',
    color: '#FFF5E1',
    popular: false,
  },
  {
    id: 4,
    name: 'Chocolate Fudge',
    description: 'Rich Belgian chocolate with fudge swirls',
    price: '$5.49',
    category: 'ice-cream',
    color: '#8B4513',
    popular: true,
  },
  {
    id: 5,
    name: 'Salted Caramel',
    description: 'Sweet caramel with a hint of sea salt',
    price: '$5.49',
    category: 'ice-cream',
    color: '#D4A574',
    popular: false,
  },
  {
    id: 6,
    name: 'Cookie Dough',
    description: 'Vanilla ice cream loaded with cookie dough chunks',
    price: '$5.99',
    category: 'ice-cream',
    color: '#E8D5C4',
    popular: true,
  },
  // Ice Pops
  {
    id: 7,
    name: 'Mango Tango',
    description: 'Tropical mango bursting with natural fruit flavor',
    price: '$2.99',
    category: 'ice-pop',
    color: '#FFD93D',
    popular: true,
  },
  {
    id: 8,
    name: 'Berry Blast',
    description: 'Mixed berries - strawberry, blueberry, raspberry',
    price: '$2.99',
    category: 'ice-pop',
    color: '#A28BFE',
    popular: false,
  },
  {
    id: 9,
    name: 'Watermelon Wave',
    description: 'Refreshing watermelon perfect for hot summer days',
    price: '$2.49',
    category: 'ice-pop',
    color: '#FF6B9D',
    popular: true,
  },
  {
    id: 10,
    name: 'Lemonade Chill',
    description: 'Tangy lemonade frozen to icy perfection',
    price: '$2.49',
    category: 'ice-pop',
    color: '#FFF176',
    popular: false,
  },
  {
    id: 11,
    name: 'Coconut Lime',
    description: 'Creamy coconut with a zesty lime twist',
    price: '$3.49',
    category: 'ice-pop',
    color: '#A7FFEB',
    popular: false,
  },
  {
    id: 12,
    name: 'Pineapple Paradise',
    description: 'Sweet tropical pineapple chunks frozen on a stick',
    price: '$2.99',
    category: 'ice-pop',
    color: '#FFE082',
    popular: true,
  },
]

const filteredItems = ref(menuItems)

const handleFilterChange = (filter) => {
  activeFilter.value = filter
  if (filter === 'all') {
    filteredItems.value = menuItems
  } else {
    filteredItems.value = menuItems.filter((item) => item.category === filter)
  }
}
</script>

<template>
  <div class="menu-page">
    <MenuHeader />
    <MenuFilter :active-filter="activeFilter" @filter-change="handleFilterChange" />
    <MenuGrid :items="filteredItems" />
  </div>
</template>

<style scoped>
.menu-page {
  width: 100%;
  min-height: 100vh;
  background: linear-gradient(to bottom, #fff5f7 0%, #ffffff 100%);
}
</style>
