<script setup lang="ts">
import previewSection from './sections/preview-section.vue'
import reviewSection from './sections/review-section.vue'
import garantSection from './sections/garant-section.vue'
import servicesSection from './sections/services-section.vue'
import projectsSection from './sections/projects-section.vue'
</script>

<template>
  <div class="content">
    <div class="preview-section"><preview-section /></div>

    <div class="review-section side-padding"><review-section /></div>

    <div class="garant-section side-padding"><garant-section /></div>

    <div class="services-section side-padding"><services-section /></div>

    <div class="projects-section side-padding"><projects-section /></div>

    <div>Lorem ipsum dolor sit amet, consectetur adipisicing elit.</div>
  </div>
</template>

<style lang="scss" scoped>
.side-padding {
  padding: 0 3%;
}
</style>
