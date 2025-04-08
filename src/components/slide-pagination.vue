<script setup lang="ts">
interface IProps {
  count: number
  active: number
}

defineProps<IProps>()
</script>

<template>
  <div class="items">
    <div
      class="item"
      :class="{ active: index == active }"
      v-for="index in count"
      :key="index"
      @click="$emit('switchActive', index)"
    >
      {{ index }}
    </div>
  </div>
</template>

<style lang="scss" scoped>
.items {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 100%;
  margin-right: 20px;
}

.item {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 6vw;
  max-width: 94px;
  height: 56px;
  color: var(--cl-primary);
  border: 1px solid var(--cl-primary);
  transition: color 0.3s ease, border-color 0.3s ease;
  cursor: pointer;
  user-select: none;

  &.active {
    color: var(--cl-secondary);
    border: 1px solid var(--cl-secondary);
  }
}
</style>
