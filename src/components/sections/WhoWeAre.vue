<template>
  <div class="who-we-are-main">
    <DogFace 
    class="dog-face-block"
    />
    <OurPromise 
    class="our-promise-block"
    />
  </div>
</template>

<script>
import DogFace from '@/components/DogFace';
import OurPromise from '@/components/OurPromise';
  export default {
    components: {
      DogFace,
      OurPromise,
    }
  }
</script>

<style scoped>
.who-we-are-main {
  background-color: #F5F5F5;
  position: relative;
  z-index: 1;
}
.dog-face-block {
  margin: 0 auto;
  transform: translate(0, -70px);
  padding-bottom: 130px;
}
.our-promise-block {
  margin: 0 auto;
  color: black;
  padding-bottom: 122px;
}
@media screen and (max-width: 810px) {
  .dog-face-block {
    padding-bottom: 15%;
  }
}
@media screen and (max-width: 500px) {
.dog-face-block {
  margin: 0 auto;
  transform: translate(0, -30px);
  }
}
@media screen and (max-width: 450px) {
  .dog-face-block {
    padding-bottom: 40%;
  }
}
</style>