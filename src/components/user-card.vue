<script setup lang="ts">
const cardInfo = {
  id: 0,
  name: 'Юрий Архипов',
  role: 'Директор ТОО "Copyland"',
  review:
    'Разработана очень удобная система приема и обработки заказов, с ней реально высвобождается огромное количество ресурсов.',
  rating: 5,
  date: '21.06.28',
  userAvatar: 'https://ucarecdn.com/b879c200-500c-4402-ac21-3de2cdca612c/',
  userAvatarAltName: 'avatar',
}
</script>

<template>
  <div class="container">
    <img
      class="avatar"
      :src="cardInfo.userAvatar"
      :alt="cardInfo.userAvatarAltName"
    />
    <p class="name">{{ cardInfo.name }}</p>
    <p class="role">{{ cardInfo.role }}</p>
    <p class="review">{{ cardInfo.review }}</p>
    <div class="rating">
      <img
        class="star"
        v-for="i in cardInfo.rating"
        :key="i"
        src="../assets/star.svg"
        alt="star"
      />
    </div>
    <div class="date">{{ cardInfo.date }}</div>
  </div>
</template>

<style lang="scss" scoped>
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  max-width: 420px;
  text-align: center;
}

.avatar {
  width: 100px;
  height: 100px;
  margin-bottom: 15px;
  border-radius: 50%;
}

.name {
  font-size: 20px;
  text-transform: uppercase;
}

.role {
  margin-bottom: 30px;
  font-size: 18px;
  font-weight: 300;
}

.review {
  margin-bottom: 40px;
  font-size: 16px;
  font-weight: 300;
}

.star {
  width: 25px;
  height: 25px;
}

.date {
  font-size: 16px;
  font-weight: 300;
}
</style>
