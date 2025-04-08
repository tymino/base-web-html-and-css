<script setup lang="ts">
import { ref } from 'vue'

import titleForSection from '../components/title-for-section.vue'
import slidePagination from '../components/slide-pagination.vue'
import slideContent from '../components/slide-content.vue'

const activeSlide = ref(1)

const switchActiveSlide = (index: number) => (activeSlide.value = index)
</script>

<template>
  <div class="container">
    <div class="title">
      <title-for-section>Наш процесс работы</title-for-section>
    </div>
    <div class="content">
      <div class="pagination">
        <slide-pagination
          @switch-active="switchActiveSlide"
          :count="7"
          :active="activeSlide"
        />
      </div>

      <slide-content
        imageSrc="https://ucarecdn.com/5a556d3e-6c7c-4715-9128-e7f2ebe384cb/"
        imageAlt="book"
        descTitle="1. Мастерская открытий"
        descBody="Мы придаем первостепенное значение пониманию и документированию входов, предпочтений клиентов, дизайна и брендов. И проясните все открытые моменты, чтобы получить точное и ясное представление о целях как клиентов, так и проекта. Мы работаем в рамках совместного подхода с участием  заинтересованных сторон, чтобы согласовать бизнес-процессы."
      />
    </div>
  </div>
</template>

<style lang="scss" scoped>
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 130px;
}

.content {
  display: flex;
  margin: 60px 0;
}
</style>
