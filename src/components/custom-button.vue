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
  black: 'text-black',
  green: 'text-green',
  white: 'text-white',
}

const baseStyle = ''

const typeStyle = computed(() => {
  switch (props.view) {
    case 'primary':
      return `w-[160px] h-[50px] bg-primary-light text-secondary ${
        colorToTailwind[props.color]
      }`
    case 'secondary':
      return `w-[100px] h-[40px] border border-primary-light text-primary-light ${
        colorToTailwind[props.color]
      }`
    default:
      return ''
  }
})
</script>

<template>
  <button :class="`${baseStyle} ${typeStyle}`" :type="type">
    {{ name }}
  </button>
</template>
