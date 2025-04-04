<script setup lang="ts">
import titleForSection from '../components/title-for-section.vue'
import infoCard from '../components/info-card.vue'

const cardInfo = [
  {
    id: 0,
    title: 'Разработка мобильных приложений',
    description:
      'Мы создаем мобильные приложения, которые нравятся пользователям. Воспользовавшись преимуществами искусственного интеллекта, машинного обучения, Интернета вещей и других высокотехнологичных технологий для создания шедевров приложений, которые сохранятся.',
    icon: 'mobile.svg',
  },
  {
    id: 1,
    title: 'Разработка программного обеспечения',
    description:
      'Уже более 10 лет мы освоили лучшие веб-технологии для реализации проектов, в которые вложены инвестиции. Надежный лидер рынка в разработке высокопроизводительных веб-интерфейсов для любого бизнеса.',
    icon: 'computer.svg',
  },
  {
    id: 2,
    title: 'Разработка веб приложений',
    description:
      'Мы не только идем в ногу с «тенденциями дизайна», но и ориентируемся на пользователей, что делает наши услуги наиболее эффективными на всем рынке. Превосходство с 2010 года. Создадим идеальное веб приложение именно для вас.',
    icon: 'internet.svg',
  },
]
</script>

<template>
  <div class="container">
    <div class="title">
      <title-for-section>Основные услуги</title-for-section>
    </div>
    <div class="card-items">
      <div class="item" v-for="info in cardInfo" :key="info.id">
        <info-card
          :title="info.title"
          :description="info.description"
          :icon="info.icon"
        />
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.container {
  display: flex;
  flex-direction: column;
}

.title {
  margin-top: 6%;
  margin-bottom: 40px;
  text-align: center;
}

.card-items {
  display: flex;
  justify-content: space-between;
  margin: 0 auto;
  width: 100%;
  max-width: 1400px;
}
</style>
