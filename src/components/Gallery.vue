<template>
  <MainPanel :bluPanelActive="true" class="gallery">
    <Title class="gallery__title" :themeWhite="true">
      <template v-slot:title>
        GALLERY & LIVE STREAMS
      </template>
      <template v-slot:subtitle>
        Check out our hard workers
      </template>
    </Title>
    <Carusel class="gallery__carusel"/>
  </MainPanel>
</template>

<script>
import MainPanel from '@/components/MainPanel';
import Title from '@/components/Title';
import Carusel from '@/components/Carusel';
export default {
  components: {
    MainPanel,
    Title,
    Carusel,
  }
}
</script>

<style scoped>
.gallery {
  box-sizing: border-box;
  background-color: #5D62B5;
  border-radius: 40px;
  padding-left: 87px;
  padding-right: 87px;
  padding-top: 100px;
  position: relative;
  height: 700px;
}
.gallery__title {
  margin-bottom: 55px;
}
.gallery__carusel {
  position: absolute;
  left: 8.5%;
}
@media screen and (max-width: 1024px) {
  .gallery {
    height: 500px;
  }
  .gallery__carusel {
    left: 1%;
    width: 98%;
  }
}
@media screen and (max-width: 600px) {
  .gallery {
    padding-left: 50px;
    padding-right: 50px;
    padding-top: 60px;
  }
}
</style>