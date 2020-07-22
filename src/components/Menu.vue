<template>
  <div class="menu">
    <ul class="menu__container">
      <li class="menu__item">
        Services 
        <img src="../assets/expand.png" class="menu__expand-button"> 
        <Dropdown 
        class="dropdown"
        :theme="'desktop'"/>
      </li>
      <li class="menu__item">Specials</li>
      <li class="menu__item">Facilities</li>
      <li class="menu__item">Reviews</li>
      <li class="menu__item">
        Shop 
        <img src="../assets/expand.png" class="menu__expand-button"> 
        <Dropdown 
        class="dropdown"
        :theme="'desktop'"/>
      </li>
      <li class="menu__item">About</li>
    </ul>
    <img src="../assets/close.png" class="menu__icon">
  </div>
</template>

<script>
import Dropdown from '@/components/Dropdown';
  export default {
    components: {
      Dropdown,
    },
  }
</script>

<style scoped>
.menu {
  margin-top: 28px;
  height: 60px;
  background-color: white;
  box-sizing: border-box;
  padding: 10px 40px;
  border-radius: 10px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: relative;
}
.menu__container {
  margin: 0;
  padding: 0;
  list-style: none;
  display: flex;
}
.menu__item {
  position: relative;
  margin-right: 37px;
  font-weight: bold;
  font-size: 14px;
  line-height: 22px;
  text-align: center;
  color: black;
}
.menu__item:hover .dropdown {
  display: block;
}
@media screen and (max-width: 755px) {
  .menu {
    display: none;
  }
}
</style>