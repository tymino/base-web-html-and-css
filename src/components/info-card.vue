<script setup lang="ts">
import moreInfoButton from './more-info-button.vue'

interface IProps {
  title: string
  description: string
  icon: string
}

defineProps<IProps>()
</script>

<template>
  <div class="container">
    <div class="title">{{ title }}</div>
    <div class="description">{{ description }}</div>
    <div class="link"><more-info-button /></div>
    <div class="bookmark">
      <img :src="icon" alt="icon" />
    </div>
  </div>
</template>

<style lang="scss" scoped>
.container {
  position: relative;
  display: flex;
  justify-content: space-between;
  max-width: 340px;
  height: 480px;
  padding: 80px 40px 40px 40px;
  border-radius: 20px;
  box-shadow: 0px 0px 6px 2px var(--cl-shadow);

  text-align: left;
  overflow: hidden;
}

.bookmark {
  position: absolute;
  content: '';
  top: -60px;
  left: 170px;
  display: flex;
  justify-content: center;
  align-items: flex-end;
  width: 300px;
  height: 160px;

  padding: 20px;
  background: var(--cl-secondary);

  transform: rotate(45deg);

  & img {
    transform: rotate(-45deg);
  }
}

.title {
  font-size: 20px;
  width: 80%;
}

.description {
  font-size: 14px;
}

.link {
  width: 100%;
  box-shadow: none;
}
</style>
