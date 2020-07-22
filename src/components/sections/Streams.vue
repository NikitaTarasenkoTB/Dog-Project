<template>
  <div class="page">
    <Gallery class="streams__gallery"/>
    <OurCustomers />
  </div>
</template>

<script>
import Gallery from '@/components/Gallery.vue';
import OurCustomers from '@/components/OurCustomers';
export default {
  components: {
    Gallery,
    OurCustomers,
  }
}
</script>

<style scoped>
.streams {

}
.streams__gallery {
  margin: 0 auto;
  transform: translate(0, -70px);
  padding-bottom: 130px;
}
</style>