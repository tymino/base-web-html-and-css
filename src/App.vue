<script setup lang="ts">
import previewSection from './sections/preview-section.vue'
import reviewSection from './sections/review-section.vue'
import garantSection from './sections/garant-section.vue'
import servicesSection from './sections/services-section.vue'
import projectsSection from './sections/projects-section.vue'
import processingSection from './sections/processing-section.vue'
import techSection from './sections/tech-section.vue'
import messageSection from './sections/message-section.vue'
import footerSection from './sections/footer-section.vue'
</script>

<template>
  <div class="content">
    <div class="preview-section"><preview-section /></div>

    <div class="review-section side-padding"><review-section /></div>

    <div class="garant-section side-padding"><garant-section /></div>

    <div class="services-section side-padding"><services-section /></div>

    <div class="projects-section side-padding"><projects-section /></div>

    <div class="processing-section side-padding"><processing-section /></div>

    <div class="tech-section side-padding"><tech-section /></div>

    <div class="message-section"><message-section /></div>

    <div class="footer-section side-padding"><footer-section /></div>
  </div>
</template>

<style lang="scss" scoped>
.side-padding {
  padding: 0 3%;
}
</style>
