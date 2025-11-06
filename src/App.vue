<script setup>
import { RouterView } from 'vue-router'
import TheHeader from './components/TheHeader.vue'
</script>

<template>
  <div class="wrapper">
    <TheHeader />
  </div>

  <RouterView />
</template>

<style scoped></style>
