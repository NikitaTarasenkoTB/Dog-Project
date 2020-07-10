<template>
  <div id="app" class="app">
    <Intro />
    <WhoWeAre />
    <DogWithBall />
    <OurServices />
    <router-view />
  </div>
</template>

<script>
// import {mapGetters, mapActions, mapMutations} from 'vuex';
import Intro from '@/components/sections/Intro';
import WhoWeAre from '@/components/sections/WhoWeAre';
import DogWithBall from '@/components/sections/DogWithBall';
import OurServices from '@/components/sections/OurServices';

export default {
  name: 'App',
  components: {
    Intro,
    WhoWeAre,
    DogWithBall,
    OurServices,
  }

}
</script>

<style>
body {
  margin: 0;
}
#app {
  font-family: 'Roboto', Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: white;
}
</style>
