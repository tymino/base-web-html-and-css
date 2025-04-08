<script setup lang="ts">
import moreInfoButton from './more-info-button.vue'

interface IProps {
  imageSrc: string
  imageAlt: string
  descTitle: string
  descBody: string
}

defineProps<IProps>()
</script>

<template>
  <div class="wrapper">
    <img class="main-image" :src="imageSrc" :alt="imageAlt" />
    <div class="description">
      <div class="title">{{ descTitle }}</div>
      <div class="body">{{ descBody }}</div>
      <div class="footer"><more-info-button /></div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.wrapper {
  display: flex;
}

// .main-image {
// }

.description {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: flex-start;
  margin-left: 40px;
  padding: 20px 0;
  max-width: 700px;
}

.title {
  font-size: 40px;
  text-transform: uppercase;
}

.body {
  font-size: 18px;
}
</style>
