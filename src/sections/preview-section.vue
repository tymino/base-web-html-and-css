<script setup lang="ts">
import mainLogo from '../components/main-logo.vue'
import navMenu from '../components/nav-menu.vue'
import customButton from '../components/custom-button.vue'
</script>

<template>
  <div class="container">
    <div class="bg-image-overlay">
      <img
        class="bg-image"
        src="https://ucarecdn.com/761233c4-7224-418d-b151-ea7bc1196250/"
        alt=""
      />
    </div>

    <div class="content">
      <div class="header">
        <main-logo />
        <nav-menu />
      </div>
      <div class="body">
        <h1 class="body__title">
          компания по разработке программного обеспечения
        </h1>
        <div class="body__button">
          <custom-button
            type="button"
            view="secondary"
            color="white"
            name="запросить консультацию"
          />
        </div>
        <div class="body__arrow">
          <svg
            width="42"
            height="72"
            viewBox="0 0 42 72"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              d="M21 -18V71M21 71L1 44.6296M21 71L41 44.6296"
              stroke="white"
              stroke-width="2"
            />
          </svg>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.container {
  position: relative;
  overflow: hidden;
}

.bg-image {
  position: relative;
  display: block;
  width: 100%;
  height: auto;
  margin-top: -200px;
  object-fit: cover;
  object-position: 0 200px;
  z-index: -10;

  &-overlay::after {
    position: absolute;
    content: '';
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(var(--color-primary), 0.65);
  }
}

.content {
  position: absolute;
  content: '';
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}

.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 14px 6%;
  background: rgba(var(--color-secondary), 0.12);
}

.body {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100%;

  &__title {
    max-width: 820px;
    margin-bottom: 60px;
    color: var(--cl-neutral);
    font-size: 47px;
    font-weight: 200;
    text-align: center;
  }

  &__button {
    display: flex;
    justify-content: center;
    margin-bottom: 48px;
  }

  &__arrow {
    color: var(--cl-neutral);
    text-align: center;
  }
}
</style>
