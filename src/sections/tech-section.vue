<script setup lang="ts">
import titleForSection from '../components/title-for-section.vue'

const iconLinks = [
  'https://ucarecdn.com/83a57cbc-eb76-4b0f-9e51-41c2d1c8bab5/',
  'https://ucarecdn.com/dd80002f-5b41-4e9d-bec8-d7adee83025e/',
  'https://ucarecdn.com/a97e2ecc-3825-443f-8a94-6a912d1c4fe9/',
  'https://ucarecdn.com/73891360-1f89-459a-afe0-557b32c23250/',
  'https://ucarecdn.com/f93eac32-ea69-4624-8480-2e63ba3c57e4/',
  'https://ucarecdn.com/dc706670-8c6e-48ea-8da7-68a00f293806/',
  'https://ucarecdn.com/dcc3592f-38a8-4a86-92d2-245520938e18/',
  'https://ucarecdn.com/e0153d68-cd09-464a-9bd1-3f22d214b0e6/',
  'https://ucarecdn.com/1e5cc959-92d1-4695-baf7-f019e0f635cd/',
  'https://ucarecdn.com/cf959e95-f193-4626-a1da-11d850f7d3ab/',
  'https://ucarecdn.com/e90892c4-45bd-408c-9940-920d3e734952/',
  'https://ucarecdn.com/9d183eee-4ec3-4ca4-8871-fff04fcb14e0/',
  'https://ucarecdn.com/fe8632d0-0764-4f60-9d1e-dbc87ff2749e/',
  'https://ucarecdn.com/29cde8bb-ee6b-4f0c-b573-fb60ad1fc936/',
  'https://ucarecdn.com/6964928d-71a1-4b94-a6d5-eb378992b5bf/',
]
</script>

<template>
  <div class="container">
    <div class="title">
      <title-for-section>Инструменты и технологии</title-for-section>
    </div>

    <div class="items">
      <img
        class="icon"
        v-for="link in iconLinks"
        :key="link"
        :src="link"
        alt="icon"
      />
    </div>
  </div>
</template>

<style lang="scss" scoped>
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 100px;
  margin-bottom: 140px;
}

.items {
  display: flex;
  flex-wrap: wrap;
  gap: 40px;
  margin-top: 60px;
  padding: 0 20px;
  max-width: 1400px;
}

.icon {
  width: auto;
  height: 120px;
  margin: 0 auto;
}
</style>
