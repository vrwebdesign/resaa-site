<style lang="scss" scoped>
.wrapper {
  text-align: center;
  margin-top: 60px;
  display: flex;
  flex-direction: column;
  align-items: center;
  @include media(md-and-up) {
    padding: 0 110px;
  }
}

.item-wrapper {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  margin: 20px -16px;
  padding: 0 20px;
  max-width: 1065px;
  @include media(md-and-up) {
    padding: 0;
  }
  .item {
    width: 100%;
    @include media(md-and-up) {
      width: 250px;
    }
    height: 250px;
    background: #fff;
    margin: 16px;
    box-shadow: 0 5px 5px rgba(0, 0, 0, 0.16);
    border-radius: 16px;
    display: flex;
    flex-direction: column;
    align-items: center;
    &--image {
      background: #f0f0f0;
      border-radius: 100%;
      overflow: hidden;
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 4px;
      width: 110px;
      height: 110px;
      margin-top: 20px;
      img {
        max-width: 100%;
      }
    }
    &--title {
      color: #212121;
      font-weight: 500;
      margin: 8px 12px;
      font-size: 16px;
    }
    &--description {
      font-weight: 300;
      color: #4a4a4a;
      padding: 0 12px;
      text-align: center;
      font-size: 13px !important;
    }
  }
}
</style>
<template>
  <section id="Symptoms">
    <div class="wrapper">
      <h2>علائم شایع کرونا</h2>
      <p>اگر هر یک از این علائم را دارید می توانید با تست در منزل از سلامت یا ابتلای خود مطلع شوید</p>
      <div class="item-wrapper">
        <div class="item" v-for="(item, index) in items" :key="index">
          <div class="item--image">
            <v-img :src="item.image" :alt="item.title" />
          </div>
          <h3 class="item--title">{{item.title}}</h3>
          <p class="item--description">{{item.description}}</p>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  data() {
    return {
      items: [
        {
          image: "/img/corona-test/fever.svg",
          title: "تب بالا",
          description:
            "یکی از اولین علائمی که در کرونا شناسایی شد و در عموم مبتلایان دیده شده است تب 38 تا 40 درجه است."
        },
        {
          image: "/img/corona-test/dry_cough.svg",
          title: "سرفه خشک",
          description:
            "سرفه ها می تواند بسته به شخص کم یا زیاد باشد اما عموما بدون مخاط در گلو و بعضا همراه با سوزش هستند."
        },
        {
          image: "/img/corona-test/breath.svg",
          title: "تنگی نفس",
          description:
            "مشکل و سنگینی در هنگام نفس کشیدن خصوصا در هنگام خواب که ممکن است با حساسیت فصلی اشتباه گرفته شود. "
        },
        {
          image: "/img/corona-test/tiredness.svg",
          title: "خستگی",
          description:
            "خستگی مفرط بدون ارتباط به حجم فعالیت روزانه ی شما از علائمی است که برای بی علامت ترین افراد هم اتفاق افتاده است."
        },
        {
          image: "/img/corona-test/musle_pain.svg",
          title: "درد عضلات",
          description:
            "کوفتگی و درد بدن در پهلوها، کمر، پاها و استخوان ها می تواند از علائم کرونا باشد."
        },
        {
          image: "/img/corona-test/headache.svg",
          title: "سر درد",
          description:
            "در روزهای اول ممکن است سردرد  و درد پشت چشم تجربه کنید که ممکن است با سرماخوردگی فصلی و سینوزیت اشتباه بگیرید."
        }
      ]
    };
  }
};
</script>