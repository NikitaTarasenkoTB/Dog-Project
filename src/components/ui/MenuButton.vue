<template>
  <button 
  :class="['hamburger', 'hamburger--spin', {isActive: isButtonActive}]" 
  type="button"
  @click="$emit('isMobileMenuShown')">
    <span class="hamburger-box">
      <span class="hamburger-inner"></span>
    </span>
  </button> 
</template>

<script>
  export default {
    props: ['isButtonActive'],
    methods: {
      output() {
        console.log(this.isButtonActive);
      }
    }
  }
</script>

<style scoped>
.hamburger {
  z-index: 2;
}
</style>