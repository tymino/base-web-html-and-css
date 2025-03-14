<script setup lang="ts">
import CustomButton from './components/custom-button.vue'
</script>

<template>
  <div class="text-3xl text-red-600">Hello Vue</div>
  <custom-button type="button" view="primary" color="black" name="Click me" />
  <div class="bg-black">
    <img
      src="https://ucarecdn.com/a97e2ecc-3825-443f-8a94-6a912d1c4fe9/"
      alt=""
    />
  </div>
  <div class="flex flex-col justify-center items-center mt-5">
    <h1>Title title</h1>
    <p>Hello</p>
  </div>
</template>
