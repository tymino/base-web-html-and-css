<script setup lang="ts">
import mainLogo from '../components/main-logo.vue'
</script>

<template>
  <div class="container">
    <div class="column-logo">
      <main-logo :is-dark="true" />
      <p>Алматы, Жамбыла 111</p>
    </div>

    <div class="column-contacts">
      <div class="phones">
        <img src="../assets/phone.svg" alt="phone" />
        <div>
          <p>+7 (727) 334-21-45</p>
          <p>+7 (707) 998-93-90</p>
        </div>
      </div>
      <div class="mail-social">
        
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.container {
  margin-top: 130px;
}

.column-logo {
  display: flex;
  flex-direction: column;
  margin-bottom: 40px;
}

.column-phones {
}
</style>
