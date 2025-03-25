<script setup lang="ts">
const navMenuNames = [
  'главная',
  'услуги',
  'как мы работаем',
  'портфолио',
  'о нас',
  'контакты',
]
</script>

<template>
  <div class="wrapper">
    <ul class="container">
      <li class="item" v-for="name in navMenuNames" :key="name">{{ name }}</li>
    </ul>
  </div>
</template>

<style lang="scss" scoped>
.wrapper {
  width: 60%;
  // border: 1px solid red;
}

.container {
  display: flex;
  justify-content: space-between;
  list-style: none;
  color: var(--cl-neutral);
}

.item {
  margin: 0 5px;
  cursor: pointer;
  transition: all 0.2s ease-in-out;

  &::first-letter {
    text-transform: uppercase;
  }

  &:hover {
    color: var(--cl-primary);
  }

  &:nth-child(2) {
    position: relative;

    &::before {
      position: absolute;
      top: 0;
      left: calc(100% + 4px);
      content: '˅';
    }

    &:hover::before {
      transform: rotate(180deg);
      transition: transform 0.6s ease;
    }
  }
}
</style>
