<script setup lang="ts">
interface IProps {
  srcIcon: string
  items: string[]
  isSmall?: boolean
}

defineProps<IProps>()
</script>

<template>
  <div class="contact-list">
    <img class="icon" :src="srcIcon" alt="icon" />
    <div class="wrapper">
      <p
        class="item"
        :class="{ small: isSmall }"
        v-for="item in items"
        :key="item"
      >
        {{ item }}
      </p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.contact-list {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.icon {
  width: 26px;
  height: auto;
  margin-right: 10px;
}

.wrapper {
  display: flex;
  flex-direction: column;
}

.item {
  margin-bottom: 10px;
  color: var(--cl-primary);
  font-size: 18px;
  line-height: 30px;
  text-transform: uppercase;

  &.small {
    font-size: 13px;
    text-transform: uppercase;
  }
}
</style>
