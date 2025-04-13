<script setup lang="ts">
interface IProps {
  names: string[]
}

defineProps<IProps>()
</script>

<template>
  <div class="link-list">
    <a class="link" v-for="name in names" :key="name" href="#">{{ name }}</a>
  </div>
</template>

<style lang="scss" scoped>
.link-list {
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.link {
  color: var(--cl-primary);
  font-size: 18px;
  font-weight: 300;
  text-decoration: none;
}
</style>
