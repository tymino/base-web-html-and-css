<script setup lang="ts">
import { computed } from 'vue'

interface IProps {
  name: string
  view: 'primary' | 'secondary'
  color: 'black' | 'green' | 'white'
  type: 'button' | 'submit'
}
const props = defineProps<IProps>()

const buttonStyle = computed(
  () => `button button__${props.view}--${props.color}`,
)
</script>

<template>
  <button :class="buttonStyle" :type="type">
    {{ name }}
  </button>
</template>

<style lang="scss" scoped>
@mixin button-primary($textColor, $BgColor) {
  color: $textColor;
  background: $BgColor;
  border-color: $BgColor;
  box-shadow: 4px 4px 4px var(--cl-shadow);
}

@mixin button-secondary($color) {
  color: $color;
  border-color: $color;
}

.button {
  min-width: 120px;
  padding: 10px 0px;
  background: transparent;
  border-radius: 14px;
  border-style: solid;
  border-width: 2px;

  font-size: 16px;
  cursor: pointer;

  &__primary {
    &--black {
      @include button-primary(var(--cl-neutral), var(--cl-primary));
    }
    &--green {
      @include button-primary(var(--cl-neutral), var(--cl-secondary));
    }
    &--white {
      @include button-primary(var(--cl-primary), var(--cl-neutral));
    }
  }
  &__secondary {
    &--black {
      @include button-secondary(var(--cl-primary));
    }
    &--green {
      @include button-secondary(var(--cl-secondary));
    }
    &--white {
      @include button-secondary(var(--cl-neutral));
    }
  }

  &:hover {
    transform: translateY(1px);
  }
}
</style>
