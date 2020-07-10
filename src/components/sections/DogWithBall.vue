<template>
  <div class="dog-with-ball">
    <div class="dog-with-ball__image">
      <div class="dog-with-ball__container">
        <h2 class="dog-with-ball__title">Nemo enim ipsam voluptatem quia voluptas in proident</h2>
        <Button class="dog-with-ball__button" />
      </div>
    </div>
  </div>
</template>

<script>
import Button from '@/components/ui/Button';
export default {
  components: {
    Button,
  }
}
</script>

<style scoped>
.dog-with-ball {
  background-color: #29C3BE;
}
.dog-with-ball__image {
  margin: 0 auto;
  width: 1440px;
  height: 500px;
  background-image: url('../../assets/images/dog-with-ball-image.png');
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  display: flex;
  flex-direction: column;
  align-items: flex-end;
}
.dog-with-ball__container {
  padding-top: 112px;
  padding-right: 14%;
}
.dog-with-ball__title {
  margin: 0;
  max-width: 411px;
  font-weight: 900;
  font-size: 36px;
  line-height: 42px;
  margin-bottom: 42px;
}
@media screen and (max-width: 1440px) {
  .dog-with-ball__image {
    width: 100%;
  }
}
@media screen and (max-width: 1024px) {
  .dog-with-ball__container {
    padding-top: 112px;
    padding-right: 5%;
  }
}
@media screen and (max-width: 480px) {
  .dog-with-ball__container {
    padding-left: 5%;
  }
}
</style>