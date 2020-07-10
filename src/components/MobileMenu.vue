<template>
  <div class="mobile-menu">
    <ul class="mobile-menu__container">
      <li
        @click="showDropdownService" 
        class="mobile-menu__item">
        Services 
        <img src="../assets/expand.png" class="menu__expand-button"> 
        <transition name="mobile-menu">
          <Dropdown
            v-if="isShownDropdownService"
            class="dropdown"
            :theme="'mobile'"/>
        </transition>
        </li>
      <li class="mobile-menu__item">Specials</li>
      <li class="mobile-menu__item">Facilities</li>
      <li class="mobile-menu__item">Reviews</li>
      <li
        @click="showDropdownShop" 
        class="mobile-menu__item">
        Shop 
        <img src="../assets/expand.png" class="menu__expand-button"> 
        <transition name="mobile-menu">
          <Dropdown
            v-if="isShownDropdownShop"
            class="dropdown"
            :theme="'mobile'"/>
        </transition>
        </li>
      <li class="mobile-menu__item">About</li>
    </ul>
    <div class="mobile-menu__about">
      <div class="mobile-menu__about-container">
        <img src="../assets/time.png" alt="Время" class="mobile-menu__image">
        <ul class="mobile-menu__about-info">
          <li class="mobile-menu__about-info-title">BOARDING HOURS</li>
          <li class="mobile-menu__about-info-data">Mon - Sat: 7:00 am - 6:00 pm</li>
        </ul>
      </div>
      <div class="mobile-menu__about-container">
        <img src="../assets/phone.png" alt="Телефон" class="mobile-menu__image">
        <ul class="mobile-menu__about-info">
          <li class="mobile-menu__about-info-title">CALL US</li>
          <li class="mobile-menu__about-info-data">(555) Pup-Cares</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
import Dropdown from '@/components/Dropdown';
  export default {
    components: {
      Dropdown,
    },
    data() {
      return {
        isShownDropdownService: false,
        isShownDropdownShop: false,
      }
    },
    methods: {
      showDropdownService() {
        this.isShownDropdownService = !this.isShownDropdownService;
      },
      showDropdownShop() {
        this.isShownDropdownShop = !this.isShownDropdownShop;
      }
    }
  }
</script>

<style scoped>
.mobile-menu {
  position: fixed;
  top: 0;
  right: 0;
  width: 60vw;
  height: 100vh;
  background-color: #5D62B5;
  z-index: 1;
  opacity: 1;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
.mobile-menu__container {
  margin: 0;
  padding: 0;
  list-style: none;
  display: flex;
  flex-direction: column;
  padding-top: 80px;
  width: 60%;
  padding-left: 50px;
}
.mobile-menu__item {
  position: relative;
  font-weight: bold;
  font-size: 37px;
  line-height: 42px;
  border-bottom: 1px solid white;
  margin-bottom: 20px;
}
.mobile-menu__about {
  padding-left: 30px;
}
.mobile-menu__about-container {
  display: flex;
  justify-content: flex-start;
  margin-bottom: 20px;
}
.mobile-menu__about-info {
  margin: 0;
  padding: 0;
  list-style-type: none;
  font-weight: bold;
  font-size: 12px;
  line-height: 22px;
  margin-left: 10px;
}
.mobile-menu__image {
  width: 24px;
  height: 24px;
}
.mobile-menu-enter, .mobile-menu-leave-to {
  height: 0;
}
.mobile-menu-enter-active, .mobile-menu-leave-active  {
  transition: height .2s ease-in-out;
}
@media screen and (max-width: 600px){
  .mobile-menu {
    width: 100vw;
  }
}
</style>