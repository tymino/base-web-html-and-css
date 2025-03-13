<template>
  <button
    class="py-2 px-4 rounded-md text-white"
    :style="{ borderColor: borderColor }"
  >
    {{ name }}
  </button>
</template>

<script setup lang="ts">
defineProps<{
  name: string
  borderColor: string
}>()
</script>
