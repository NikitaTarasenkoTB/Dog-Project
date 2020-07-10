<template>
  <MainPanel :bluPanelActive="true">
    <div class="dog-face">
      <Title class="dog-face__title" :themeWhite="true">
        <template v-slot:title>
          Who we are
        </template>
        <template v-slot:subtitle>
          Nemo enim ipsam voluptatem quia voluptas in proident
        </template>
      </Title>
      <p class="dog-face__info">Ut enim ad minima veniam, quis nostrum exercitationem ullam corporis suscipit laboriosam, nisi ut aliquid ex ea commodi consequatur. Quis autem vel eum iure reprehenderit qui in ea voluptate velit esse quam nihil molestiae consequatur, vel illum qui dolorem eum fugiat quo voluptas nulla pariatur.</p>
      <img src="../assets/images/dog-face.png" alt="Собака" class="dog-face__image">
    </div>
  </MainPanel>
</template>

<script>
import MainPanel from '@/components/MainPanel';
import Title from '@/components/Title';
export default {
  components: {
    MainPanel,
    Title,
  }
}
</script>

<style scoped>
.dog-face {
  box-sizing: border-box;
  background-color: #5D62B5;
  border-radius: 40px;
  padding-left: 87px;
  padding-right: 87px;
  padding-top: 100px;
  position: relative;
  height: 700px;

  background-image: url('../assets/images/blob.png');
  background-repeat: no-repeat;
  background-position: left -14px top 270px;
}
.dog-face__title {
  margin-bottom: 36px;
}
.dog-face__info {
  margin: 0;
  font-size: 16px;
  line-height: 24px;
  margin-bottom: 6%;
}
.dog-face__image {
  width: 846px;
  position: absolute;
  left: 8.5%;
}
@media screen and (max-width: 1020px) {
  .dog-face__image {
    left: 0;
    width: 100%;
  }
}
@media screen and (max-width: 600px) {
  .dog-face {
    padding-left: 60px;
    padding-right: 60px;
    padding-top: 90px;
  }
}
@media screen and (max-width: 350px) {
  .dog-face {
    padding-left: 40px;
    padding-right: 40px;
    padding-top: 40px;
  }
}
</style>