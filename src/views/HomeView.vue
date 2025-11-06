<!-- HOME PAGE (views/HomeView.vue) -->
<script setup>
import HeroSection from '@/components/HeroSection.vue'
import FeaturedProducts from '@/components/FeaturedProducts.vue'
import AboutPreview from '@/components/AboutPreview.vue'
import CTASection from '@/components/CTASection.vue'
</script>

<template>
  <div class="home-page">
    <HeroSection />
    <FeaturedProducts />
    <AboutPreview />
    <CTASection />
  </div>
</template>

<style scoped>
.home-page {
  width: 100%;
}
</style>
