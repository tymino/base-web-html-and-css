<script setup lang="ts">
import userCard from '../components/user-card.vue'
</script>

<template>
  <div class="container">
    <div class="review">
      <user-card />
    </div>
    <div class="form"></div>
  </div>
</template>

<style lang="scss" scoped>
.container {
}

.review {
  padding: 60px 0;
  background: rgba(var(--color-secondary), 0.1);
}
</style>
