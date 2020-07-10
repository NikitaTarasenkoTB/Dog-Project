<template>
  <div :class="['card', {cardColumn: cardColumn}]">
    <img :src="url" :class="['card__image', {card__imageRow: cardRow}, {card__imageColumn: cardColumn}]">
    <div :class="[{crad__container: cardColumn}]">
      <h3 class="card__title">
        {{title}}
      </h3>
      <p class="card__text">
        {{text}}
      </p>
    </div>
  </div>
</template>

<script>
  export default {
    props: ['url', 'title', 'text', 'cardRow', 'cardColumn'],
  }
</script>

<style scoped>
.card {
  display: flex;
  max-width: 324px;
  color: #4B4B4B;
}
.cardColumn {
  align-items: center;
  flex-direction: column;
  background-color: #fff;
  border-radius: 20px;
  box-sizing: border-box;
  padding: 50px 44px 49px 44px;
  box-shadow: none;
}
.crad__container {
  display: flex;
  align-items: center;
  flex-direction: column;
}
.card__image {
  width: 63px;
  height: 63px;
  margin-right: 23px;
}
.card__imageRow {
  margin-right: 23px;
}
.card__imageColumn {
  margin-bottom: 33px;
}
.card__title {
  margin: 0;
  font-weight: 900;
  font-size: 19px;
  line-height: 26px;
  margin-bottom: 20px;
  color: #F2726F;
}
.card__text {
  margin: 0;
  font-size: 16px;
  line-height: 24px;
}
.cardColumn:hover {
  box-shadow: 0px 16px 24px rgba(38, 38, 38, 0.2), 0px 8px 16px rgba(38, 38, 38, 0.24);
  transition: box-shadow .2s ease-in;
}
</style>