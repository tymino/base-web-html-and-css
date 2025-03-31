<script setup lang="ts">
const reviewNames = [
  { id: 0, header: '98%', desc: 'завершенных проектов успешно' },
  { id: 1, header: '30', desc: 'календарных дней до первого релиза' },
  { id: 2, header: '5+', desc: 'дней от идеи до готовой концепции' },
  { id: 3, header: '+20%', desc: 'к эффективности бизнеса' },
]
</script>

<template>
  <div class="container">
    <div class="review" v-for="{ id, header, desc } in reviewNames" :key="id">
      <h2 class="title">{{ header }}</h2>
      <p class="desc">{{ desc }}</p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.container {
  display: flex;
  justify-content: center;
  margin: 12% auto;
}

.review {
  display: flex;
  flex-direction: column;
  align-items: center;
  max-width: 300px;
  padding: 0 20px;
  letter-spacing: 2px;
  text-align: center;

  &:not(:last-child) {
    border-right: 2px solid var(--cl-secondary);
  }
}

.title {
  margin-bottom: 10px;
  font-size: 48px;
  font-weight: 600;
}

.desc {
  font-size: 16px;
  font-weight: 400;
}
</style>
