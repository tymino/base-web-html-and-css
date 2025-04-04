<script setup lang="ts">
import titleForSection from '../components/title-for-section.vue'
import moreInfoButton from '../components/more-info-button.vue'
import customButton from '../components/custom-button.vue'
</script>

<template>
  <div class="container">
    <div class="title">
      <title-for-section>Проекты</title-for-section>
    </div>
    <div class="content">
      <svg
        class="arrow arrow-left"
        width="14"
        height="26"
        viewBox="0 0 14 26"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path d="M13 25L1 13L13 0.999999" stroke="currentColor" />
      </svg>
      <img
        class="main-image"
        src="https://ucarecdn.com/26b4a8e2-88ae-42b0-81f7-90bcf30ad7ef/"
        alt="book"
      />
      <div class="description">
        <div class="header">Компания по производству фотокниг Fototeca</div>
        <div class="body">
          Программное решение, автоматизирующее производство изделий – от
          создания дизайна до выдачи клиенту. Была создана система, которая
          позволяет профессиональному фотографу – клиенту компании — формировать
          изделие (фотокнигу) в нужном формате и виде, оплатить и сразу передать
          заказ в производство.
        </div>
        <div class="footer"><more-info-button /></div>
      </div>
      <svg
        class="arrow arrow-right"
        width="14"
        height="26"
        viewBox="0 0 14 26"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path d="M1 1L13 13L1 25" stroke="currentColor" />
      </svg>
    </div>
    <customButton
      name="Посмотреть все проекты"
      type="button"
      view="primary"
      color="black"
    />
  </div>
</template>

<style lang="scss" scoped>
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 130px;
}

.content {
  display: flex;
  margin: 60px 0;
}

.arrow {
  align-self: center;
  min-width: 14px;
  color: var(--cl-primary);
  transition: color 0.3s ease;
  cursor: pointer;

  &-left {
    margin-right: 20px;
  }

  &-right {
    margin-left: 20px;
  }

  &:hover {
    color: var(--cl-secondary);
  }
}

.description {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: flex-start;
  margin-left: 40px;
  padding: 20px 0;
  max-width: 700px;
}

.header {
  font-size: 40px;
  text-transform: uppercase;
}

.body {
  font-size: 18px;
}
</style>
