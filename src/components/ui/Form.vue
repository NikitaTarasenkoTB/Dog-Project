<template>
  <form class="form">
    <h2 class="form__title">Make an appointment</h2>
    <input 
      class="form__input form__input-area form__input_name"
      type="text"
      name="name"
      placeholder="Name"
      minlength="2"
      maxlength="30"
      required
    >
    <input 
      class="form__input form__input-area form__input_email"
      type="email"
      name="email"
      placeholder="Email"
      required
    >
    <input 
      class="form__input form__input-area form__input_number"
      type="tel"
      name="phone-number"
      placeholder="Phone Number"
      required
    >
    <input 
      class="form__input form__input-area form__input_services"
      type="text"
      name="services"
      placeholder="Select Service"
    >
    <textarea 
      class="form__textarea form__input-area"
      name="about" 
      placeholder="Tell us about your puppers include his/her name"
    ></textarea>
    <Button 
      class="form__button"
      type="submit"
    />
  </form>
</template>

<script>
import Button from '@/components/ui/Button';
export default {
  components: {
    Button,
  }
}
</script>

<style scoped>
.form {
  padding: 76px 57px;
  max-width: 585px;
  background: #5D62B5;
  border-radius: 40px;
  box-shadow: 0px 16px 24px rgba(38, 38, 38, 0.2), 0px 8px 16px rgba(38, 38, 38, 0.24);

  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-template-rows: auto;
  grid-template-areas: 
    "title title"
    "name email"
    "number services"
    "textarea textarea"
    "button button";
  grid-gap: 22px;
  box-sizing: border-box;
}
.form__title {
  margin: 0;
  max-width: 470px;
  margin-bottom: 20px;
  font-weight: 900;
  font-size: 36px;
  line-height: 42px;
  text-align: center;
  grid-area: title;
  justify-self: center;
}
.form__input {
  height: 48px;
}
.form__textarea {
  max-width: 100%;
  height: 180px;
  grid-area: textarea;
  padding-top: 17px;
}
.form__input-area {
  background-color: #5D62B5;
  border-radius: 8px;
  outline: none;
  border: 1px solid white;
  opacity: 0.8;
  color: white;
  padding-left: 24px;

  font-family: Roboto;
  font-style: normal;
  font-weight: normal;
  font-size: 16px;
  line-height: 24px;
  letter-spacing: 0.15px;
}
.form__input_name {
  grid-area: name;
}
.form__input_email {
  grid-area: email;
}
.form__input_number {
  grid-area: number;
}
.form__input_services {
  grid-area: services;
}
.form__input::placeholder, .form__textarea::placeholder {
  color: white;
}
.form__button {
  grid-area: button;
  justify-self: end;
}
@media screen and (max-width: 600px) {
  .form {
    padding: 16% 11%;
      grid-template-areas: 
      "title title"
      "name name"
      "email email"
      "number number"
      "services services"
      "textarea textarea"
      "button button";
  }
  .form__input {
    height: 40px;
  }
  .form__textarea {
    height: 100px;
  } 
}
</style>