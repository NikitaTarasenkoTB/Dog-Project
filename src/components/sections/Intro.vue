<template>
  <div class="intro">
    <div class="intro__container">
      <Header />
      <Menu />
      <h1 class="intro__title">Premier dog boarding, daycare & day spa</h1>
      <Button class="intro__button" />
    </div>
  </div>
</template>

<script>
import Header from '@/components/Header';
import Menu from '@/components/Menu';
import Button from '@/components/ui/Button';

export default {
  name: 'App',
  components: {
    Header,
    Menu,
    Button
  }
}
</script>

<style scoped>
.intro__container {
  margin: 0 auto;
  max-width: 1020px;
}
.intro {
  background-image: url('../../assets/images/intro-image.png');
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  z-index: 9;
}
.intro__title {
  margin-top: 12.6%;
  max-width: 583px;
  font-weight: 900;
  font-size: 56px;
  line-height: 56px;
}
.intro__button {
  margin-top: 48px;
  padding-bottom: 25.6%;
}

@media screen and (max-width: 1130px) {
  .intro__container {
    max-width: calc(100% - 100px);
  }
}
@media screen and (max-width: 450px) {
  .intro__title {
    font-size: 36px;
    line-height: 46px;
  }
}
</style>