<style lang="scss" scoped>
.wrapper {
  display: flex;
  flex-direction: column-reverse;
  justify-content: center;
  margin-top: 10px;
  @include media(md-and-up) {
    margin-top: 90px;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
  }
}
.image {
  height: 250px;
  display: flex;
  justify-content: center;
  align-items: center;
  @include media(md-and-up) {
    height: auto;
    flex: 0 0 50%;
  }
}
.text {
  margin-top: 20px;
  flex: 0 0 50%;
  text-align: center;
  @include media(md-and-up) {
    text-align: right;
  }
  h1 {
    color: #212020;
    font-size: 30px;
    margin-bottom: 16px;
    @include media(md-and-up) {
      font-size: 38px;
      margin-bottom: 30px;
    }
  }
  p {
    text-align: center;
    color: #717171;
    @include media(md-and-up) {
      text-align: justify;
      max-width: 400px;
      margin-bottom: 40px;
    }
  }
  .button-wrapper {
    .v-btn {
      width: calc(100% - 16px);
      height: 40px;
      @include media(md-and-up) {
        width: 180px;
      }
      &.reserve-btn {
        background: linear-gradient(to right, #28db9a, #0ec7e5);
        box-shadow: 0 3px 3px rgba(0, 0, 0, 0.16);
      }
    }
  }
}
</style>
<template>
  <section id="FirstFord">
    <div class="wrapper">
      <div class="text">
        <h1>تست کرونا در منزل</h1>
        <p>اگر مشکوک به کرونا هستید همین امروز می توانید در منزل خود تست کرونا دهید. متخصصین آزمایشگاه های شناخته شده و دارای مجوز از جمله بیمارستان مهراد، آزمایشگاه تهران طب و میلاد در کمتر از 24 ساعت اعزام شده و در محل مورد نظر شما نمونه گیری میکنند و نتیجه ی آزمایش را در سریع ترین زمان به صورت آنلاین به شما اعلام می کنند.</p>
        <div class="button-wrapper">
          <v-btn
            v-scroll-to="{el:'#FormBox',offset: 0, duration:1000 }"
            class="reserve-btn"
            dark
            round
            depressed
          >رزرو تست کرونا</v-btn>
          <!-- <v-btn
            to="/corona-test/tracking"
            class="reserve-btn"
            dark
            round
            depressed
          >پیگیری تست کرونا</v-btn>-->
          <v-btn href="tel:02174471300" color="primary" outline round>تماس با پشتیبانی</v-btn>
        </div>
      </div>
      <div class="image">
        <v-img height="100%" position="center top"  alt="تست کرونا در منزل" :src="$device.isDesktop?'/img/corona-test/top_img@2x.png':'/img/corona-test/top_img@1x.png'" />
      </div>
    </div>
  </section>
</template>
<script>
export default {};
</script>
