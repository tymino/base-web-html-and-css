<script setup lang="ts">
defineProps<{ isDark?: boolean }>()
</script>

<template>
  <div class="wrapper">
    <img
      class="icon"
      src="https://ucarecdn.com/b4157a46-7c83-475d-afd0-e2d490c29bbd/"
      alt="logo"
    />
    <p class="text" :class="{ dark: isDark }">devcloud solutions</p>
  </div>
</template>

<style lang="scss" scoped>
.wrapper {
  display: flex;
  justify-content: center;
  align-items: center;

  .icon {
    width: auto;
  }

  .text {
    margin-left: 6px;
    color: var(--cl-neutral);
    font-size: 20px;
    font-weight: bold;
    text-transform: uppercase;

    &.dark {
      color: var(--cl-primary);
    }
  }
}
</style>
