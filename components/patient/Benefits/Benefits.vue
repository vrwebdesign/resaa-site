<template>
  <div class="benefits-section-patient-container">
    <!-- <img class="benefits-section-patient-curve" src="./sec-2-bg@2x2.png" /> -->
    <h2 class="section-title" id="element">چرا مشاوره پزشکی در سامانه رسا؟</h2>
    <p class="section-description">مشاوره پزشکی رسا چه مزایایی دارد؟</p>
    <div class="benefits-container">
      <div class="benefits-text">
        <h3 class="benefits-text-title">مزایای استفاده از سامانه رسا</h3>
        <ul class="benefits-list">
          <li>تماس مستقیم با پزشک بدون نیاز به شماره همراه ایشان</li>
          <li>صرفه جویی در وقت و هزینه بدون حضور در مطب</li>
          <li>اطلاع رسانی وضعیت پزشک برای مکالمات بعدی</li>
          <li>
            <a v-scroll-to="{ el: '#doctors', offset: -50 }">معرفی پزشکان</a> از طریق وب سایت و اپلیکیشن رِسا
          </li>
          <!-- <li>
            شارژ آسان حساب از طریق اپلیکیشن رِسا و یا کد
            <a href="tel:*500*25#">USSD</a>
          </li>-->
          <li>
            شارژ آسان حساب از طریق
            <router-link :to="{name:'charge'}">همین سایت</router-link>
          </li>
        </ul>
        <div class="benefits-button-container">
          <!-- <v-btn
            to="/patient/register"
            id="benefitsRegister"
            color="yellow darken-2"
            class="benefits-signup-button"
            round
          >ثبت نام رایگان</v-btn>-->
          <resaaButton id="benefitsRegister" theme="dark" to="/patient/register">ثبت نام رایگان</resaaButton>
          <v-btn
            class="benefits-download-button"
            id="showVideo"
            color="secondary"
            outline
            round
            @click="$emit('openVideo')"
          >نمایش ویدئو</v-btn>
          <!-- <v-btn
            class="benefits-download-button"
            v-scroll-to="{ el: '#download', offset: -50 , duration: 1500}"
            outline
            round
            color="secondary"
          >دریافت اپلیکیشن</v-btn>-->
        </div>
      </div>
      <div class="image">
        <img src="./mockup.jpg" alt="مزایای استفاده از سامانه رسا" />
      </div>
    </div>
  </div>
</template>

<script>
import resaaButton from "~/components/resaa-button.vue";
export default {
  components: {
    resaaButton
  }
};
</script>

<style lang="scss" scoped>
.benefits-section-patient-curve {
  width: 100%;
  position: relative;
  top: -95px;
  height: 110px;
}

.benefits-section-patient-container {
  background-color: white;
  padding: 80px 0;
}

.section-title {
  background-image: linear-gradient(240deg, #3de0cb, #0dc9f0);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  font-weight: 500;
  text-align: center;
  font-size: 1.75rem;
  margin-bottom: 15px;
}

.section-description {
  color: #777590;
  text-align: center;
  font-style: normal;
  font-size: 1.075rem;
  font-weight: 300;
}

.benefits-container {
  margin-top: 20px;
  display: flex;
  flex-direction: row-reverse;
  justify-content: space-evenly;
  align-items: center;
  width: 1200px;
  max-width: 100%;
  margin: 0 auto;
  .image {
    img {
      width: 850px;
      max-width: 100%;
    }
  }
}

.benefits-text {
  // background-image: url("ptrn.png");
  background-repeat: no-repeat;
  background-position: right;
  background-size: contain;
  direction: rtl;
  margin-right: -70px;
  z-index: 9;
}

.benefits-text-title {
  color: #757779;
  font-weight: 500;
  font-size: 1.475rem;
  margin-bottom: 10px;
}

.benefits-list {
  direction: rtl;
  list-style: none;
  padding: 10px;
  margin: 0;
  text-align: right;

  li {
    line-height: 30px;
    color: #777590;
    @include media(sm) {
      font-size: 1rem;
    }
    a {
      color: #00aae2;
      text-decoration: underline;
      cursor: pointer;
    }
  }

  li::before {
    position: relative;
    top: 5px;
    margin-left: 10px;
    vertical-align: middle;
    content: "•";
    font-size: 40px;
    padding: 0;
    color: #4cdbc4;
  }
}

.benefits-button-container {
  display: flex;

  flex-direction: row;
}

.benefits-signup-button {
  width: 174px;
  box-shadow: 0 5px 7.5px 0 rgba(255, 206, 70, 0.3);
  color: #545456;
  background-color: #febe10;
}

.benefits-download-button {
  width: 174px;
  box-shadow: 0 5px 7.5px 0 rgba(72, 229, 202, 0.2);
  border-width: 2px;
}

@media only screen and (max-width: 1000px) {
}

@media only screen and (max-width: 900px) {
  .benefits-container {
    flex-direction: column;
    .benefits-text {
      margin-right: 0;
    }
    img {
      margin-top: 20px;
    }
  }
}

@media only screen and (max-width: 600px) {
  .benefits-section-patient-curve {
    height: 30px;
    top: -30px;
  }

  .benefits-container {
    img {
      // padding: 20px 20px 30px;
      margin: 0;
    }
  }

  .benefits-text {
    text-align: center;
  }
}

@media only screen and (max-width: 500px) {
}

@media only screen and (max-width: 400px) {
  .benefits-section-patient-container {
    padding: 0 0 20px;
  }

  .benefits-button-container {
    flex-direction: column;
    align-items: center;

    div {
      margin: 5px;
    }
  }

  .section-title {
    font-size: 1.75rem;
  }

  .section-description {
    font-size: 1.175rem;
  }

  .benefits-text-title {
    font-size: 1.8rem;
    margin: 0;
  }

  .benefits-text {
    font-size: 1.2rem;
  }
}

@media only screen and (max-width: 300px) {
  .benefits-container {
    img {
      display: none;
    }
  }
}
</style>
