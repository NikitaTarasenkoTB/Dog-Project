<template>
  <div class="page">
    <div class="carusel__slider" @click="changeSlide($event)">
      <p ref="slider0" id="slider1" class="carusel__slidertext carusel__slidertext_enabled">Gallery1</p>
      <p ref="slider1" id="slider2" class="carusel__slidertext">Gallery2</p>
      <p ref="slider2" id="slider3" class="carusel__slidertext">Gallery3</p>
      <p ref="slider3" id="slider4" class="carusel__slidertext">Gallery4</p>
    </div>
    <div class="myCarusel">
      <b-carousel
        id="carousel-fade"
        fade
        ref="myCarousel"
        v-model="slide"
        :interval="0"
        background="#ababab"
        img-width="846"
        img-height="480"
        no-touch
        style="text-shadow: 1px 1px 2px #333;"
      >
        <b-carousel-slide>
          <template v-slot:img>
            <img
              class="d-block img-fluid w-100 carusel-image"
              width="846"
              height="480"
              src="https://picsum.photos/1024/480/?image=52"
              alt="image slot"
            >
          </template>
        </b-carousel-slide>

        <b-carousel-slide>
          <template v-slot:img>
            <img
              class="d-block img-fluid w-100 carusel-image"
              width="846"
              height="480"
              src="https://picsum.photos/1024/480/?image=54"
              alt="image slot"
            >
          </template>
        </b-carousel-slide>

        <b-carousel-slide>
          <template v-slot:img>
            <img
              class="d-block img-fluid w-100 carusel-image"
              width="846"
              height="480"
              src="https://picsum.photos/1024/480/?image=58"
              alt="image slot"
            >
          </template>
        </b-carousel-slide>

        <b-carousel-slide>
          <template v-slot:img>
            <img
              class="d-block img-fluid w-100 carusel-image"
              width="846"
              height="480"
              src="https://picsum.photos/1024/480/?image=55"
              alt="image slot"
            >
          </template>
        </b-carousel-slide>
      </b-carousel>
    </div>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        slide: 0,
        nextSlide: 0,
        isThisSlide: true,
        sliding: null
      }
    },
    methods: {
      changeSlide(event) {
        this.nextSlide = Number(event.target.id.charAt(event.target.id.length - 1)) - 1;
        this.$refs[`slider${this.slide}`].classList.remove('carusel__slidertext_enabled');
        this.slide = this.nextSlide;
        event.target.classList.add('carusel__slidertext_enabled');
        this.$refs.myCarousel.setSlide(this.nextSlide);
      }
    },
  }
</script>

<style scoped>
.page {
  width: 846px;
}
.carusel-image {
  width: 846px;
  height: 480px;
}
.myCarusel {
  width: 100%;
  border-radius: 40px;
  box-shadow: 0px 16px 24px rgba(38, 38, 38, 0.2), 0px 8px 16px rgba(38, 38, 38, 0.24);
  overflow: hidden;
}
.carusel__slider {
  display: flex;
  flex-direction: row;
  border-bottom: 1px solid rgba(255, 255, 255, .5);
  width: 100%;
  margin-bottom: 50px;
}
.carusel__slidertext_enabled {
  border-bottom: 3px solid white;
}
.carusel__slidertext {
  margin: 0;
  padding-bottom: 15px;
  font-weight: bold;
  font-size: 16px;
  line-height: 24px;
  text-align: center;
  letter-spacing: 0.15px;
  width: calc(100% / 4);
  cursor: pointer;
}
@media screen and (max-width: 860px) {
  .page {
    width: 100%;
  }
  .myCarusel {
    width: 100%;
    height: auto;
  }
  .carusel-image {
    height: auto;
  }
}
</style>