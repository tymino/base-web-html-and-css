<script setup lang="ts">
import customButton from '../components/custom-button.vue'
</script>

<template>
  <div class="container">
    <img
      class="image"
      src="https://ucarecdn.com/83398f66-832a-4a52-9930-0549e372be61/"
      alt="tolpa"
    />
    <div class="description">
      <div class="header">Гарантируем качество и выполнение в сроки</div>
      <div class="body">
        <p>
          Мы просто умеем разрабатывать то, что нужно. То, что будет работать!
        </p>
        <div class="button">
          <customButton
            name="Запросить консультацию"
            type="button"
            view="primary"
            color="black"
          />
        </div>
      </div>

      <div class="footer">
        С 2010 года профессионально разрабатываем успешные мобильные и
        веб-решения, индивидуальные програ ммные решения, информационные системы
        и ПО для бизнеса, которые повышают эффективность бизнеса.
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.container {
  display: flex;
  justify-content: space-between;
}
.image {
  width: auto;
  max-height: 600px;
}

.description {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  padding: 40px 60px 20px;

  text-align: center;
}

.header {
  position: relative;
  max-width: 530px;
  margin-bottom: 40px;
  font-size: 40px;
  font-weight: bold;

  &::after {
    content: '”';
    position: absolute;
    top: -26px;
    right: -54px;

    font-family: 'Helvetica Neue', sans-serif;
    color: lightgray;
    font-size: 120px;
  }

  &::before {
    content: '“';
    position: absolute;
    bottom: -86px;
    left: -40px;

    font-family: 'Helvetica Neue', sans-serif;
    color: lightgray;
    font-size: 120px;
  }
}

.body {
  p {
    max-width: 500px;

    font-size: 20px;
    font-weight: 400;
    letter-spacing: 1px;
  }

  .button {
    margin-top: 14px;
  }
}

.footer {
  max-width: 600px;
  font-size: 13px;
  font-weight: 300;
  letter-spacing: 1px;
}
</style>
