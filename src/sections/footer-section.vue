<script setup lang="ts">
import mainLogo from '../components/main-logo.vue'
import contactList from '../components/contact-list.vue'
import linkList from '../components/link-list.vue'

const phones = ['+7 (727) 334-21-45', '+7 (707) 998-93-90']
const mails = ['info@devcloud.kz']
const whatapp = ['Whatsapp']
const telegram = ['telegram']
const links1 = ['Главная', 'Портфолио', 'Услуги']
const links2 = ['Процессы', 'О компании', 'Контакты']
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

    <div class="column-links-1">
      <link-list :names="links1" />
    </div>
    <div class="column-links-2">
      <link-list :names="links2" />
    </div>

    <div class="column-arrow">
      <svg
        width="34"
        height="57"
        viewBox="0 0 34 57"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          d="M17 57.3999L17 1.08562M17 1.08562L33 17.7713M17 1.08562L1 17.7713"
          stroke="black"
        />
      </svg>
    </div>
    <div class="copyright">
      © Devcloud Solutions, Inc. 2021. We love our users!
    </div>
  </div>
</template>

<style lang="scss" scoped>
.container {
  position: relative;
  display: flex;
  justify-content: space-between;
  margin: 60px auto;
  padding: 120px 0;
}

.column-logo {
  display: flex;
  flex-direction: column;
  align-items: end;
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

// .column-arrow {
// }

.copyright {
  position: absolute;
  bottom: 0;
  right: 0;
  width: 100%;
  height: 80px;
  padding: 30px 20px 0 0;
  border-top: 1px solid rgba(0, 0, 0, 0.4);
  font-size: 15px;
  font-weight: 300;
  text-align: end;
}
</style>
