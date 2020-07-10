<template>
  <header class="header">
    <div class="header__logo-container">
      <img src="../assets/logo.png" alt="Логотип" class="header__logo">
      <MenuButton 
      :isButtonActive="isButtonActive"
      class="header__menu-button"
      @isMobileMenuShown="isMobileMenuShown"
      />
      <transition name="mobileMenu">
        <MobileMenu 
        v-if="isButtonActive"
        />
      </transition>
    </div>
    <div class="header__about">
      <div class="header__container">
        <img src="../assets/time.png" alt="Время" class="header__image">
        <ul class="header__about-info">
          <li class="header__about-info-title">BOARDING HOURS</li>
          <li class="header__about-info-data">Mon - Sat: 7:00 am - 6:00 pm</li>
        </ul>
      </div>
      <div class="header__container">
        <img src="../assets/phone.png" alt="Телефон" class="header__image">
        <ul class="header__about-info">
          <li class="header__about-info-title">CALL US</li>
          <li class="header__about-info-data">(555) Pup-Cares</li>
        </ul>
      </div>
      <Button 
      @buttonClick="buttonClick"
      class="header__button" /> 
    </div>
  </header>
</template>

<script>
import Button from '@/components/ui/Button';
import MenuButton from '@/components/ui/MenuButton';
import MobileMenu from '@/components/MobileMenu'
export default {
  components: {
    Button,
    MenuButton,
    MobileMenu,
  },
  data() {
    return {
      isButtonActive: false,
    }
  },
  methods: {
    buttonClick() {
      console.log('clicked!');
    },
    isMobileMenuShown() {
      this.isButtonActive = !this.isButtonActive;
    }
  }
}
</script>

<style scoped>
.header {
  padding-top: 26px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.header__about {
  display: flex;
  justify-content: flex-end;
}
.header__about-info {
  margin: 0;
  padding: 0;
  list-style-type: none;
  font-weight: bold;
  font-size: 12px;
  line-height: 22px;
}
.header__container {
  display: flex;
  margin-right: 30px;
}
.header__image {
  width: 24px;
  height: 24px;
  margin-right: 10px;
}
.header__menu-button {
  display: none;
}
.mobileMenu-enter, .mobileMenu-leave-to {
  width: 0;
}
.mobileMenu-enter-active, .mobileMenu-leave-active  {
  transition: width .2s ease-in-out;
}
@media screen and (max-width: 950px) {
  .header {
    flex-direction: column;
    align-items: flex-start;
  }
  .header__about {
    width: 100%;;
    margin-top: 40px;
    justify-content: space-around;
  }
}
@media screen and (max-width: 755px) {
  .header__about {
    display: none;
  }
  .header__logo-container {
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .header__menu-button {
  display: block;
  } 
}
@media screen and (max-width: 450px) {
  .header__logo {
    width: 100px;
  }
}
</style>