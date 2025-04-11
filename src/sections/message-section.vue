<script setup lang="ts">
import userCard from '../components/user-card.vue'
import questionForm from '../components/question-form.vue'
</script>

<template>
  <div class="container">
    <div class="review">
      <user-card />
    </div>
    <div class="form">
      <question-form />
    </div>
  </div>
</template>

<style lang="scss" scoped>
.container {
  display: flex;
}

.review {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 40%;
  padding: 60px 0;
  background: rgba(var(--color-secondary), 0.1);
}

.form {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 60%;
  padding: 60px 0;
  background: linear-gradient(
    to right,
    rgb(var(--color-secondary)),
    rgba(var(--color-secondary), 0.6)
  );
}
</style>
