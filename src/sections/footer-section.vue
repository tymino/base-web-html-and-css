<script setup lang="ts">
import mainLogo from '../components/main-logo.vue'
import contactList from '../components/contact-list.vue'

const phones = ['+7 (727) 334-21-45', '+7 (707) 998-93-90']
const mails = ['info@devcloud.kz']
const whatapp = ['Whatsapp']
const telegram = ['telegram']
</script>

<template>
  <div class="container">
    <div class="column-logo">
      <main-logo :is-dark="true" />
      <p>Алматы, Жамбыла 111</p>
    </div>

    <div class="column-contacts">
      <contact-list srcIcon="phone.svg" :items="phones" />
      <contact-list srcIcon="letter.svg" :items="mails" />
      <div class="row">
        <contact-list srcIcon="whatapp.svg" :items="whatapp" :is-small="true" />
        <contact-list
          srcIcon="telegram.svg"
          :items="telegram"
          :is-small="true"
        />
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.container {
  display: flex;

  margin-top: 130px;
  padding: 60px 0;
}

.column-logo {
  display: flex;
  flex-direction: column;
  margin-bottom: 40px;
}

.column-contacts {
  .row {
    display: flex;
  }

  div:first-child {
    margin-right: 12px;
  }
}
</style>
