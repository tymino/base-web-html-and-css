<script setup lang="ts">
interface IProps {
  count: number
  active: number
}

defineProps<IProps>()
</script>

<template>
  <div class="items">
    <div class="item" v-for="index in count" :key="index">{{ index }}</div>
  </div>
</template>

<style lang="scss" scoped></style>
