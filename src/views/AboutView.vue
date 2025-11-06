<!-- ABOUT PAGE (views/AboutView.vue) -->
<script setup>
import AboutHero from '@/components/AboutHero.vue'
import OurStory from '@/components/OurStory.vue'
import OurValues from '@/components/OurValues.vue'
import LocationSection from '@/components/LocationSection.vue'
</script>

<template>
  <div class="about-page">
    <AboutHero />
    <OurStory />
    <OurValues />
    <LocationSection />
  </div>
</template>

<style scoped>
.about-page {
  width: 100%;
}
</style>
