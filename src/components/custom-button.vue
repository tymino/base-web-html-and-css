<script setup lang="ts">
import { computed } from 'vue'

interface IProps {
  name: string
  view: 'primary' | 'secondary'
  color: 'black' | 'green' | 'white'
  type: 'button' | 'submit'
}
const props = defineProps<IProps>()

const colorToTailwind = {
  black: 'primary',
  green: 'secondary',
  white: 'neutral',
}

const typeStyle = computed(() => {
  const baseStyle = `rounded-3xl px-6 py-2 hover:brightness-105 transition border-2 border-${
    colorToTailwind[props.color]
  }`

  switch (props.view) {
    case 'primary':
      return `${baseStyle} shadow-md hover:shadow-none bg-${
        colorToTailwind[props.color]
      } text-${
        colorToTailwind[props.color] === 'neutral' ? 'primary' : 'neutral'
      }`
    case 'secondary':
      return `${baseStyle} text-${colorToTailwind[props.color]}`
    default:
      return ''
  }
})
</script>

<template>
  <button :class="typeStyle" :type="type">
    {{ name }}
  </button>
</template>
