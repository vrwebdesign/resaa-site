<template>
  <div class="download-section-patient-container" id="download">
    <h2 class="section-title">دریافت اپلیکیشن رِسا</h2>
    <p class="section-description">سازگار با سیستم عامل های اندروید، IOS و ویندوز موبایل</p>
    <div class="image-wrapper">
      <img v-lazy="mockup_img" alt="دریافت اپلیکیشن سامانه رسا" />
    </div>
    <div class="download-image-container">
      <div class="download-links">
        <div class="link" @click="openModal">
          <div class="link-icon">
            <img src="./apple.png" alt="دریافت اپلیکیشن رسا برای ای او اس" />
          </div>
          <div class="link-texts">
            <div class="link-provider-text">Available on The</div>
            <div class="link-provider">App Store</div>
          </div>
        </div>
        <!-- <div class="link" @click="openModal">
          <div class="link-icon">
            <img src="./winmobile.png" alt="دریافت اپلیکیشن رسا برای ویندوز فون" />
          </div>
          <div class="link-texts">
            <div class="link-provider-text">Download For</div>
            <div class="link-provider">WinMobile</div>
          </div>
        </div>-->
        <div class="link" @click="openModal">
          <div class="link-icon">
            <img src="./playstore.png" alt="دریافت اپلیکیشن رسا از پلی استور" />
          </div>
          <div class="link-texts">
            <div class="link-provider-text">GET IT ON</div>
            <div class="link-provider">Google Play</div>
          </div>
        </div>
        <div class="link" @click="openModal">
          <div class="link-icon">
            <img src="./cafebazar.png" alt="دریافت اپلیکیشن رسا از کافه بازار" />
          </div>
          <div class="link-texts">
            <div class="link-provider-text">دانلود از</div>
            <div class="link-provider">کافه بازار</div>
          </div>
        </div>
        <UnderDevelopment v-if="show_modal" @closeModal="closeModal"></UnderDevelopment>
      </div>
    </div>
  </div>
</template>

<script>
import UnderDevelopment from "@/components/global/under_development";
import mockup_img from "./mockup.jpg";
export default {
  components: {
    UnderDevelopment
  },
  data() {
    return {
      show_modal: false,
      mockup_img
    };
  },
  methods: {
    openModal() {
      this.show_modal = true;
    },
    closeModal() {
      this.show_modal = false;
    }
  }
};
</script>
<style lang="scss" scoped>
.image-wrapper {
  text-align: center;
  img {
    max-width: 50%;
    @include respond-to(md) {
      max-width: 80%;
    }
  }
}
@media (max-width: 900px) {
  .download-links {
    margin-top: 50px;
    width: 100% !important;
  }
}

.download-section-patient-container {
  padding: 70px 0;
  background-color: white;
}

.section-title {
  background-image: linear-gradient(240deg, #3de0cb, #0dc9f0);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  font-size: 1.75rem;
  font-weight: 500;
  text-align: center;
  margin-bottom: 10px;
}

.section-description {
  direction: rtl;
  color: #777590;
  text-align: center;
  font-style: normal;
  font-size: 1.075rem;
  font-weight: 300;
}

.download-image-container {
  padding: 0 30px;
  margin-top: 50px;
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
  align-items: center;
}

.download-links {
  justify-content: center;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;

  .link {
    direction: ltr;
    margin: 10px;
    cursor: pointer;
    padding-left: 20px;
    display: flex;
    flex-direction: row;
    align-items: center;
    width: 180px;
    height: 60px;
    border-radius: 15px;
    border: solid 2px #989cbe;
    transition: background 0.2s ease-in-out;
    &:hover {
      background: rgba(152, 156, 190, 0.2);
    }
    .link-texts {
      text-align: left;
      color: #989cbe;

      .link-provider-text {
        font-weight: 500;
        font-size: 0.875rem;
      }

      .link-provider {
        font-weight: 700;
        font-size: 1rem;
      }
    }

    .link-icon {
      margin-right: 20px;
      img {
        width: 30px;
      }
    }
  }
}

@media only screen and (max-width: 1000px) {
}

@media only screen and (max-width: 900px) {
  .download-image-container {
    margin-top: 0;
  }

  .download-links {
    margin-top: 20px;
  }
}

@media only screen and (max-width: 600px) {
}

@media only screen and (max-width: 500px) {
  .section-title {
    font-size: 2.225rem;
  }

  .section-description {
    font-size: 1.175rem;
  }
}

@media only screen and (max-width: 400px) {
  .section-description {
    padding: 0 20px;
  }
}

@media only screen and (max-width: 300px) {
}
</style>
