<template>
  <div :class="[`dropdown-${theme}`]">
    <ul :class="[`dropdown__container-${theme}`]">
      <li :class="[`dropdown__element-${theme}`]">element 1</li>
      <li :class="[`dropdown__element-${theme}`]">element 2</li>
      <li :class="[`dropdown__element-${theme}`]">element 3</li>
    </ul>
  </div>
</template>

<script>
  export default {
    props:['theme'],
  }
</script>

<style scoped>
.dropdown-desktop {
  padding-top: 10px;
  display: none;
  position: absolute;
  border-radius: 10px;
  top: 22px;
  left: -10px;
  min-width: 100px;
  background-color: white;
}
.dropdown-mobile {
  box-sizing: border-box;
  position: relative;
  /* padding-top: 10px; */
  width: 100%;
  height: 160px;
  background-color: #29C3BE;
  opacity: 1;
  overflow: hidden;
}
.dropdown__container-desktop, .dropdown__container-mobile {
  margin: 0;
  padding: 0;
  list-style: none;
}

.dropdown__element-desktop {
  margin-bottom: 10px;
}
.dropdown__element-mobile {
  padding-bottom: 10px;
  padding-left: 20px;
}
.dropdown__element-mobile:first-of-type {
  padding-top: 10px;
}
@media screen and (max-width: 350px) {
  .dropdown__element-mobile {
    padding-left: 10px;
  }
}
</style>