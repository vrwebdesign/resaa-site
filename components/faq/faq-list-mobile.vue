<style lang="scss" scoped>
section.faq-list-box {
  background: #202327;
  padding: 5px;
  border-radius: 15px;
  .faq-box {
    background-color: #1d1f23;
    color: #fff;
    border: none;
    margin: 10px;
    height: 50px;
    overflow: hidden;
    > div {
      padding: 0 20px;
    }
    &.active > div {
      background-color: #ed1163;
      background-image: url(~assets/img/Element-top-left-mobile.png);
    }
    .v-card__title {
      padding: 0;
      margin: 0;
    }
    .faq-box-show {
      background: #ed1163;
      border-radius: 0px;
    }
    .faq-box-description {
      background: #28b67b;
      padding: 10px 25px;
      border-radius: 15px;
    }
    .faq-box-description-doctor {
      display: flex;
      align-items: center;
      justify-content: center;
      background: #fff;
      color: #ddd;
      border-radius: 20px;
      width: 100%;
      margin: 0 auto;
      margin-bottom: 30px;
    }
    .faq-box-doctor-name {
      display: flex;
      flex-direction: column;
      width: 50%;
      height: 100%;
      align-items: center;
      h5 {
        color: #34ccd7;
        font-size: 1.4rem;
      }
      h6 {
        color: #626262;
        font-size: 1rem;
      }
    }
    .faq-box-doctor-ressa-code {
      display: flex;
      align-items: center;
      width: 50%;
      h6 {
        color: #b1b1b1;
        font-size: 1rem;
        span {
          color: #43e7a5;
        }
      }
    }
    .faq-box-awnser {
      padding: 30px 0;
    }
  }
}
.scroll-area-questions {
  position: relative;
  margin: auto;
  height: 200px;
  direction: ltr;
  background: rgba(0, 0, 0, 0);
}
section#question_awnser {
  .arow-down-question {
    display: flex;
    flex-direction: column;
    margin: 10px;
    .theme--light.v-icon {
      color: #ed1163;
      font-size: 50px;
      line-height: 13px;
    }
  }
  .awnser {
    background: #202327;
    background-image: url(~assets/img/element-bottom-left-gray.png);
    background-position: bottom left;
    background-repeat: no-repeat;
    background-size: auto;
    padding: 25px;
    color: #000;
    @include media(xs-only) {
      padding: 0 5px;
    }
    .user {
      display: flex;
      .user_icon {
        width: 20%;
        padding-top: 5px;
        svg {
          width: 40px;
          height: 40px;
        }
      }
      .user_speaking {
        background: #34ccd7;
        background-image: url(~assets/img/element-bottom-left-mobile.png);
        background-position: bottom left;
        background-repeat: no-repeat;
        background-size: cover;
        width: 80%;
        padding: 10px;
        color: #fff;
        font-weight: 100;
        font-size: 1.4rem;
        border-radius: 20px;
        text-align: justify;
        position: relative;
        @include media(sm) {
          padding: 10px 15px 20px;
        }
        &::before {
          content: "";
          position: absolute;
          right: -19px;
          top: 20px;
          display: block;
          border: 10px solid #000;
          border-color: transparent transparent transparent #34ccd7;
        }
        .title {
          background: #fff;
          padding: 15px 20px;
          border-radius: 20px;
          margin-bottom: 20px;
          h3 {
            color: #63e1ae;
            font-size: 1.5rem;
            margin: 0;

            @include media(xs-only) {
              font-size: 1.2rem;
            }
          }
          span {
            color: #8b8d90;
            font-size: 1rem;
          }
        }
      }
    }
    .doctor {
      display: flex;
      margin-top: 50px;
      flex-direction: row-reverse;
      .doctor_icon {
        width: 20%;
        text-align: left;
        img {
          width: 42px;
          margin-top: 5px;
          height: 42px;
          border-radius: 50%;
        }
      }
      .doctor_speaking {
        background: #28b67b;
        background-image: url(~assets/img/element-bottom-right-mobile.png);
        background-position: bottom right;
        background-repeat: no-repeat;
        background-size: cover;
        width: 80%;
        padding: 10px;
        color: #fff;
        font-weight: 100;
        font-size: 1.4rem;
        border-radius: 20px;
        text-align: justify;
        position: relative;
        @include media(sm) {
          padding: 10px 15px 30px;
        }
        &::before {
          content: "";
          position: absolute;
          left: -19px;
          top: 20px;
          display: block;
          border: 10px solid #000;
          border-color: transparent #28b67b transparent transparent;
        }
        .title {
          background: #fff;
          padding: 15px 20px;
          border-radius: 14px;
          margin-bottom: 20px;
          display: flex;
          @include media(xs-only) {
            padding: 15px 10px;
          }
          .name {
            width: 75%;
            display: flex;
            flex-direction: column;
            h3 {
              color: #63e1ae;
              font-size: 1.5rem;
              margin: 0 !important;
              @include media(xs-only) {
                font-size: 1.2rem;
              }
            }
            span {
              color: #8b8d90;
              font-size: 1rem;
              margin-top: 10px;
            }
          }
          .ressa_code {
            width: 25%;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-direction: column;
            span {
              color: #8b8d90;
              font-size: 1rem;
              margin-top: 6px;
              @include media(xs-only) {
                font-size: 0.9rem;
              }
            }
            .code {
              color: #63e1ae;
              margin-top: 12px;
            }
          }
        }
      }
    }
  }
}
</style>

<template>
  <section id="question_awnser">
    <section class="faq-list-box show-mobile">
      <h2 class="section-title">
        <img src="~assets/img/icons/faq.png" alt />
        <span>پرسش و پاسخ</span>
      </h2>
      <vue-custom-scrollbar
        class="scroll-area-questions"
        :settings="{maxScrollbarLength: 30,scrollXMarginOffset:15,suppressScrollX:true}"
      >
        <v-card
          v-for="(item,index) in items"
          :key="index"
          class="faq-box"
          :class="{active:item == active_item}"
        >
          <v-card-actions @click="active_item = item">
            <v-card-title primary-title>
              <div>
                <div class="question-title" v-html="item.question"></div>
              </div>
            </v-card-title>
          </v-card-actions>
        </v-card>
      </vue-custom-scrollbar>
    </section>
    <div class="arow-down-question" @click="goSpeaking">
      <v-icon>arrow_drop_down</v-icon>
      <v-icon>arrow_drop_down</v-icon>
    </div>
    <div v-if="active_item" class="awnser" id="speaking">
      <div class="user">
        <div class="user_icon">
          <userIcon class="svg-icon-white" width="50px" />
        </div>
        <div class="user_speaking">
          <!-- <div class="title" v-html="active_item.question">
            <h3>{{active_item.faqUserName}}</h3>
            <span>{{active_item.faqUserMail}}</span>
          </div>-->
          <div v-html="active_item.question"></div>
        </div>
      </div>
      <div class="doctor">
        <div class="doctor_icon">
          <img src="/img/doc-placeholder.png" alt />
        </div>
        <div class="doctor_speaking">
          <div class="title">
            <div class="name">
              <h3>{{active_item.respondent.fullName}}</h3>
              <span>متخصص قلب و عروق</span>
            </div>
            <div class="ressa_code">
              <span>کد رسا</span>
              <span class="code">{{active_item.respondent.subscriberNumber}}</span>
            </div>
          </div>با سلام,
          <br />
          <div v-html="active_item.answer"></div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import questions from "@/components/faq/faq.json";
import userIcon from "@/assets/svg/user.svg?inline";
export default {
  props: {
    items: {}
  },
  components: {
    userIcon
  },
  data() {
    return {
      questions,
      active_item: this.items[0]
    };
  },
  methods: {
    goSpeaking() {
      this.$scrollTo("#speaking", 1000);
    }
  }
};
</script>