<template>
  <div>
    <button 
    @click="$emit('buttonClick')"
    class="button">
      <slot>MAKE AN APPOINTMENT</slot>
    </button>
  </div>
</template>

<script>
  export default {
    
  }
</script>

<style scoped>
.button {
  background-color: #F2726F;
  border: none;
  box-shadow: 0px 16px 24px rgba(38, 38, 38, 0.2), 0px 8px 16px rgba(38, 38, 38, 0.24);
  border-radius: 8px;
  width: 210px;
  height: 48px;
  font-weight: bold;
  font-size: 12px;
  line-height: 22px;
  color: white;
}
</style>