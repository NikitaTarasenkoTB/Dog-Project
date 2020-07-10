<template>
  <div>
    <h2 class="title" :style="{color: fontColor}">
      <img 
        v-if="themeWhite"
        src="../assets/sign.png" 
        class="sign"
      >
      <img 
        v-else
        src="../assets/sign-blue.png" 
        class="sign"
      >
      <slot name="title">title</slot>
    </h2>
    <h3 class="subtitle">
      <slot name="subtitle">Nemo enim ipsam voluptatem quia voluptas in proident</slot>
    </h3>
  </div>
</template>

<script>
  export default {
    props: ['fontColor', 'themeWhite'],
  }
</script>

<style scoped>
.sign {
  width: 16px;
  height: 16px;
  margin-right: 16px;
}
.title {
  margin: 0;
  font-weight: bold;
  font-size: 12px;
  line-height: 24px;
  text-transform: uppercase;
  display: flex;
  align-items: center;
  margin-bottom: 33px;
}
.subtitle {
  margin: 0;
  font-weight: 900;
  font-size: 36px;
  line-height: 42px;
  max-width: 583px;
}
</style>