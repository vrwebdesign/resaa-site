<style lang="scss" scoped>
.wrapper {
  display: flex;
  flex-direction: column-reverse;
  justify-content: center;
  margin-top: 60px;
  @include media(md-and-up) {
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
  }
}
.image {
  flex: 0 0 50%;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 0 32px;
}
.text {
  text-align: center;
  h2 {
    margin-bottom: 20px;
  }
  p {
    color: #4a4a4a;
    max-width: 680px;
  }
}
svg {
  width: auto;
  height: auto;
}
</style>
<template>
  <section id="AntyBody">
    <div class="wrapper">
      <div class="text">
        <h2>چه کسانی باید تست آنتی بادی بدهند؟</h2>
        <p>
          این تست که به عنوان تست آزمایش خون ویروس کرونا نیز شناخته می شود متشکل
          از دو تست است.
        </p>
        <p>
          <strong>آزمایش COVID 19-IgM:</strong> وجود آنتی بادی از کلاس IgM در
          خون به این معنی است که فرد اخیرا با ویروس در تماس بوده و احتمالا ناقل
          ویروس می باشد و شاید علائم بیماری در او آشکار شود برای این فرد
          PCRتوصیه میشود.
        </p>
        <p>
          <strong>آزمایش COVID 19-IgG:</strong> وجود آنتی بادی از کلاس IgG در
          خون به این معنی است که فرد در گذشته با ویروس در تماس بوده و اگر IgG
          خون او منفی باشد احتمالا ناقل ویروس نمی باشد و بیمار نیز نیست و شاید
          تا حدودی نسبت به ویروسی که IgGخون را بالا بردهاست ایمن باشد.
        </p>
        <p>
          مثبت بودن همزمان IgMوIgGخون به این معنی است که فرد با ویروس در زمان نه
          چندان دور در تماس بوده و احتمالا ناقل بیماری می باشد برای این فرد
          آزمایش PCRتوصیه میشود.
        </p>
      </div>
      <div class="image">
        <v-img
          aspect-ratio="1"
          max-width="600px"
          :src="'/img/corona-test/antybody.png'"
          alt="چه کسانی باید تست آنتی بادی بدهند؟"
        />
      </div>
    </div>
  </section>
</template>
<script>
export default {
  components: {}
};
</script>
