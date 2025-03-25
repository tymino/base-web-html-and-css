<script setup lang="ts">
import mainLogo from '../components/main-logo.vue'
import navMenu from '../components/nav-menu.vue'
</script>

<template>
  <div class="container">
    <img
      class="bg-img"
      src="https://ucarecdn.com/761233c4-7224-418d-b151-ea7bc1196250/"
      alt=""
    />

    <div class="content">
      <div class="header">
        <main-logo />
        <nav-menu />
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.container {
  position: relative;
  overflow: hidden;
}

.bg-img {
  display: block;
  width: 100%;
  height: auto;
  margin-top: -200px;
  object-fit: cover;
  object-position: 0 200px;
  z-index: -10;
}

.content {
  position: absolute;
  content: '';
  top: 0;
  left: 0;
  width: 100%;
}

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 14px 6%;
  background-color: rgba(var(--color-secondary), 0.12);
}
</style>
