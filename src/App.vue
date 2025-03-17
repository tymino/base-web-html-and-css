<script setup lang="ts">
import CustomButton from './components/custom-button.vue'
</script>

<template>
  <div class="text-3xl text-red-600">Hello Vue</div>
  <div class="text-center mt-5 p-2 bg-red-300">
    <h2 class="text-secondary">buttons</h2>
    <div class="flex flex-row justify-center">
      <div class="mr-5">
        <custom-button
          type="button"
          view="primary"
          color="black"
          name="Click me"
        />
        <br />
        <custom-button
          type="button"
          view="primary"
          color="green"
          name="Click me"
        />
        <br />
        <custom-button
          type="button"
          view="primary"
          color="white"
          name="Click me"
        />
      </div>
      <div>
        <custom-button
          type="button"
          view="secondary"
          color="black"
          name="Click me"
        />
        <br />
        <custom-button
          type="button"
          view="secondary"
          color="green"
          name="Click me"
        />
        <br />
        <custom-button
          type="button"
          view="secondary"
          color="white"
          name="Click me"
        />
      </div>
    </div>
  </div>
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
