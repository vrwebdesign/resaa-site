<style lang="scss" scoped>
.procedure-section-doctors-container {
  background-image: linear-gradient(57deg, #33e4ea, #00b2ed);
  direction: rtl;
}

.procedure-title {
  padding-top: 60px;
  text-align: center;
  color: white;
  font-weight: 500;
  font-size: 1.75rem;
  text-shadow: 0 1px 5px rgba(12, 108, 124, 0.35);
}

.procedure-description {
  margin-top: 10px;
  direction: rtl;
  color: white;
  font-weight: normal;
  text-align: center;
  text-shadow: 0 0 3.9px rgba(12, 108, 124, 0.6);
}

.item-number {
  display: flex;
  background-color: white;
  justify-content: center;
  align-items: center;
  width: 40px;
  height: 40px;
  border-radius: 50%;
  color: #3de5be;
  font-size: 2.5rem;
  font-weight: 600;
  text-shadow: none;
  margin-bottom: 10px;
}

.item-image {
  height: 200px;
  width: auto;
}

.item-even {
  flex-direction: row-reverse !important;
}

.procedure-items-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 60px;
}

.item-text {
  max-width: 300px;
  font-size: 1.3rem;
  line-height: 25px;
  color: white;
  text-shadow: 0 0 3.9px rgba(12, 108, 124, 0.6);
}

.item-description-title {
  font-size: 1.175rem;
  font-weight: 600;
  margin-bottom: 10px;
}
.item-description {
  font-size: 1rem;
}
.item-description-link {
  cursor: pointer;
  color: white;
  border-bottom: 1px dashed;
  padding-bottom: 3px;
  font-weight: 500;
  margin: 0 4px;
}

.procedure-item {
  display: flex;
  flex-direction: row;
  min-width: 650px;
  justify-content: space-between;
  margin-bottom: 80px;
}

.procedure-button-container {
  display: flex;
  flex-direction: row;
  justify-content: center;
  padding-bottom: 60px;
}

.procedure-signup-button {
  width: 174px;
  border-width: 2px;
}

.procedure-download-button {
  width: 174px;
  color: #545456;
}

@media only screen and (max-width: 900px) {
  .procedure-item {
    min-width: 500px;
  }
}

@media only screen and (max-width: 600px) {
  .procedure-item,
  .item-odd,
  .item-even {
    min-width: unset;
    flex-direction: column !important;
    align-items: center;
  }

  .item-text {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
}

@media only screen and (max-width: 400px) {
  .procedure-button-container {
    flex-direction: column;
    align-items: center;
    padding-bottom: 50px;

    div {
      margin: 5px 0;
    }
  }

  .procedure-item {
    margin-bottom: 50px;
  }

  .item-text {
    max-width: 250px;
    margin-bottom: 10px;
    text-align: center;
  }

  .item-image {
    width: 140px;
    height: 140px;
  }
}
</style>

<template>
  <div class="procedure-section-doctors-container">
    <div class="procedure-title">روش کار رِسا</div>
    <div class="procedure-description">چطور تماس ها را مدیریت کنم؟</div>
    <div class="procedure-items-container">
      <div class="procedure-item item-odd">
        <div class="item-text">
          <div class="item-number">۱</div>
          <div class="item-description-title">ثبت نام رایگان در رِسا</div>
          <div class="item-description">
            - از طریق همین
            <router-link class="item-description-link" :to="{ name: 'doctors-register' }">سایت</router-link>و یا
            <a
              v-scroll-to="{ el: '#download', offset: -50 }"
              class="item-description-link"
            >اپلیکیشن رِسا</a>
            <br />می&#160;توانید اقدام به ثبت نام کنید.
          </div>
        </div>
        <img class="item-image" src="./Item1.png" />
      </div>
      <div class="procedure-item item-even">
        <div class="item-text">
          <div class="item-number">۲</div>
          <div class="item-description-title">تعیین وضعیت تماس</div>
          <div class="item-description">
            - برای ارتباط بیمار با پزشک، وضعیت در دسترس بودن
            <br />و بازه زمانی آن را مشخص کنید.
          </div>
        </div>
        <img class="item-image" src="./Item2D.png" />
      </div>
      <div class="procedure-item item-odd">
        <div class="item-text">
          <div class="item-number">۳</div>
          <div class="item-description-title">براحتی گفتگو کنید</div>
          <div class="item-description-list">
            <div class="item-description">- با بیمار خود بصورت مستقیم گفتگو کنید.</div>
            <div class="item-description">- هزینه تماس بصورت دقیقه ای محاسبه خواهد شد.</div>
            <div class="item-description">گزارش کارکرد از طریق سایت و اپلیکیشن قابل مشاهده است.</div>
          </div>
        </div>
        <img class="item-image" src="./Item3.png" />
      </div>
    </div>

    <div class="procedure-button-container">
      <v-btn
        color="yellow darken-2"
        class="procedure-signup-button"
        :to="{ name: 'doctors-register' }"
        round
      >ثبت نام رایگان</v-btn>
      <!-- <v-btn
        class="procedure-download-button"
        v-scroll-to="{ el: '#download', offset: -50 }"
        color="white"
        outline
        round
      >دریافت اپلیکیشن</v-btn>-->
      <!-- <router-link ></router-link> -->
    </div>
  </div>
</template>

<script>
export default {
  name: "Procedure"
};
</script>
