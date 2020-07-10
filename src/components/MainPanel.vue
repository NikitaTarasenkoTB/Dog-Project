<template>
  <div 
  :class="[{bluePanel: bluPanelActive}, {textPanel: textPanelActive}]"
  >
    <slot></slot>
  </div>
</template>

<script>
  export default {
    props: ['bluPanelActive', 'textPanelActive'],
  }
</script>

<style scoped>
.bluePanel, .textPanel {
  width: 1020px;
}
@media screen and (max-width: 1024px) {
  .bluePanel {
    width: 100%;
  }
  .textPanel {
    width: 80%;
  }
}
</style>