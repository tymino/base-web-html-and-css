<script setup lang="ts">
import titleForSection from '../components/title-for-section.vue'
import slidePagination from '../components/slide-pagination.vue'
import slideContent from '../components/slide-content.vue'
</script>

<template>
  <div class="container">
    <div class="title">
      <title-for-section>Проекты</title-for-section>
    </div>
    <div class="content">
      <div class="pagination">
        <slide-pagination :count="7" :active="1" />
      </div>

      <slide-content
        imageSrc="https://ucarecdn.com/26b4a8e2-88ae-42b0-81f7-90bcf30ad7ef/"
        imageAlt="book"
        descTitle="Компания по производству фотокниг Fototeca"
        descBody="Программное решение, автоматизирующее производство изделий – от создания
        дизайна до выдачи клиенту. Была создана система, которая позволяет
        профессиональному фотографу – клиенту компании — формировать изделие
        (фотокнигу) в нужном формате и виде, оплатить и сразу передать заказ в
        производство."
      />
    </div>
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
</style>
