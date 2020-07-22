<template>
<div class="page">
  <div class="back-dots-blob">
  <MainPanel class="appointment" :textPanelActive="true">
    <Form class="appointment__form" />
    <div class="appointment__text-container">
      <p class="appointment__text">Maxime placeat facere possimus omnis </p>
      <p class="appointment__numbers">5,700+</p>
      <p class="appointment__customers">customers served</p>
    </div>
  </MainPanel>
  </div>
</div>
</template>

<script>
import MainPanel from '@/components/MainPanel'
import Form from '@/components/ui/Form';
export default {
  components: {
    MainPanel,
    Form,
  }
}
</script>

<style scoped>
.page {
  padding-top: 130px;
  padding-bottom: 195px;
  background-image: url('../../assets/images/appointment-image.png');
  background-repeat: no-repeat;
  background-size: cover;
  background-position: right;
} 
.back-dots-blob {
  margin: 0 auto;
  max-width: 1220px;
  padding-bottom: 72px;
  background-image: url('../../assets/images/blob3.png'), 
                    url('../../assets/images/dots.png');
  background-repeat: no-repeat, no-repeat;
  background-size: auto, auto;
  background-position: top -150px left -110px, top 70px left 10px;
  position: relative;
}
.appointment {
  margin: 0 auto;
  color: white;
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
}
.appointment__text-container {
  max-width: 324px;
}
.appointment__text {
  margin: 0;
  font-weight: 900;
  font-size: 30px;
  line-height: 36px;
  text-align: center;
}
.appointment__numbers {
  margin: 0;
  font-weight: 900;
  font-size: 96px;
  line-height: 46px;
  text-align: center;
  margin-top: 55px;
  margin-bottom: 55px;
}
.appointment__customers {
  font-weight: 900;
  font-size: 19px;
  line-height: 26px;
  text-align: center;
  margin: 0;
}
@media screen and (max-width: 1024px){
  .appointment {
    justify-content: center;
  }
  .back-dots-blob {
   max-width: 700px;
  }
  .appointment__form {
    margin-bottom: 50px;
  }
}
@media screen and (max-width: 600px){
  .appointment {
   width: 95%;
  }
}
/* @media screen and (max-width: 1024px){
  .back-dots-blob {
   width: 100%;
  }
} */
</style>