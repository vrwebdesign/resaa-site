<style lang="scss" scoped>
.wrapper {
  background: #fff;
  border-radius: 16px;
  padding: 20px 10px;
  flex-direction: column;
  align-items: center;
  box-shadow: 0 5px 5px rgba(0, 0, 0, 0.16);
  display: flex;
  @include media(md-and-up) {
    padding: 20px 30px;
  }
}
h3 {
  margin-bottom: 30px;
}
// .logo-wrapper {
//   margin: 20px 0 20px;
//   display: flex;
//   justify-content: center;
//   @include media(md-and-up) {
//     margin: 20px 0 50px;
//   }
//   img {
//     max-width: calc(50% - 10px);
//     width: 120px;
//     + img {
//       margin-right: 20px;
//       @include media(md-and-up) {
//         margin-right: 40px;
//       }
//     }
//   }
// }
p {
  text-align: center;
  + p {
    // margin-top: 10px;
  }
}
</style>
<template>
  <section id="Cooperation">
    <div class="wrapper">
      <h3>روزشمار علائم ابتلا به کرونا:</h3>
      <p>از زمان آلوده شدن فرد تا بروز علائم ممکن است چندین روز طول بکشد این روز شمار از زمان بروز علائم است.</p>
      <p>
        <strong>روز اول:</strong> علائم خیلی خفیف آغاز می شود. مبتلایان در روزهای آغازین ممکن است تب، سرفه های خشک یا بعضا تنگی نفس احساس کنند. علائم برخی نیز ممکن است از جنس خستگی مفرط و درد عضلانی باشد. درصد کمی از مبتلایان ممکن است یکی دو روز قبل از بروز این علائم اسهال یا تهوع داشته باشند.
      </p>
      <p>
        <strong>روز پنجم:</strong> در موارد حاد، علائم بیمار شدید تر می شود. تنفس بیماران با مشکل همراه می شود، به خصوص افراد مسن تر و افرادی که سابقه بیمار های زمینه ای داشته باشند.
      </p>
      <p>
        <strong>روز هفتم:</strong> در ووهان اکثر کسانی که در بیمارستان بستری شدند در هفتمین روز شروع علائمشان به بیمارستان منتقل شده اند.
      </p>
      <p>
        <strong>روز هشتم:</strong> در بیماران بدحال، علائم شدید تر می شوند. مبتلایان به احتمال زیاد دچار تنگی نفس و ذات الریه یا سندرم دیسترس تنفسی حاد می شوند. در صورت بروز سندرم دیسترس تنفسی برای بیمار لوله تنفسی کار گذاشته می شود. متاسفانه اغلب کسانی که به سندرم دیسترس تنفسی دچار می شوند از دست می روند.
      </p>
      <p>
        <strong>روز دهم:</strong> در صورتی که وضعیت بیماران رو به وخامت برود، روز دهم در سیر بیماری زمانی است که بیماران به بخش مراقبت های ویژه (آی سی یو) منتقل می شوند. مشکلات گوارش و درد شکم و از دست دادن اشتها در این بیماران به شدت بیشتر می شود.
      </p>
      <p>
        شما می توانید پس از دریافت نتیجه ی تست با
        <nuxt-link
          to="/categories/medical-consultation-for-coronavirus/1141"
          target="_blank"
        >مشاوره پزشکی رایگان کرونا &nbsp;</nuxt-link>سامانه رسا بدون خروج از منزل برای درمان خود از پزشکان راهکار دریافت کنید.
      </p>
    </div>
  </section>
</template>
<script>
export default {};
</script>