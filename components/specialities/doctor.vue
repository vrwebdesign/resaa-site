<style lang="scss" scoped>
.item {
  border: 1px solid #43e7a5;
  border-radius: 20px;
  padding: 20px;
  display: flex;
  justify-content: space-between;
  background: #fcfffe;
  @include media(sm) {
    flex-direction: column;
    align-items: center;
  }
  .deactive {
    background: #fffdf8;
    border-color: #febe10;
    img {
      filter: grayscale(0.8);
    }
  }
  .image {
    border-radius: 100%;
    width: 140px;
    height: 140px;
    border: 1px solid #d4d4d4;
    padding: 10px;
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;

    .status {
      position: absolute;
      top: 2px;
      right: 8px;
    }
    img {
      max-width: 100%;
      max-height: 100%;
      border-radius: 100%;
    }
  }
  .name {
    flex: 1;
    text-align: right;
    margin-right: 20px;
    @include media(sm) {
      margin-right: 0;
      width: 100%;
      padding: 0 10px;
    }
    .doctor-name {
      font-size: 20px;
      color: #969696;
      font-weight: 500;
      margin-top: 16px;
      margin-bottom: 8px;
      @include media(sm) {
        display: block;
        text-align: center;
        font-weight: normal;
      }
    }
    .doctor-speciality {
      font-size: 16px;
      color: #9f9f9f;
      font-weight: 500;
      margin-bottom: 20px;
      @include media(sm) {
        text-align: center;
        font-weight: normal;
        font-size: 14px;
      }
    }
    .doctor-tags {
      font-size: 12px;
      color: #9f9f9f;
      font-weight: normal;
      @include media(sm) {
        display: flex;
        justify-content: space-between;
        span {
          display: flex;
          + span {
            margin-top: 6px;
          }
        }
        .success-call {
          display: flex;
          flex-direction: column;
          align-items: center;
          margin-right: 30px;
          svg {
            width: auto;
            height: auto;
            margin-bottom: 4px;
          }
          span {
            font-size: 18px;
            color: #1ad0c1;
            font-weight: 500;
          }
        }
      }
      p {
        margin-bottom: 0;
      }
    }
  }
  .price {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    text-align: center;
    font-size: 15px;
    padding: 10px 0;
    @include media(sm) {
      padding: 0;
      margin-top: 20px;
    }
    .success-call {
      span {
        color: #1ad0c1;
      }
    }
    .price-per-minute {
      color: #1ad0c1;
    }
    .select-btn {
      min-width: 160px;
      min-height: 36px;
      font-size: 13px;
      background: linear-gradient(to left, #0ec7e6, #28db9a);
      font-weight: 500;
    }
  }
}
</style>

<template>
  <section class="item" :class="{deactive:!doctor.currentlyAvailable}">
    <nuxt-link class="image" :to="`/doctors/psychology/${doctor.subscriberNumber}`">
      <div class="status">
        <component :is="doctor.currentlyAvailable?'Available':'NotAvailable'"></component>
      </div>
      <img
        v-if="doctor.imagePath"
        :key="doctor.subscriberNumber"
        v-lazy="'https://webapi.resaa.net/'+doctor.imagePath"
        :alt="`تصویر ${doctor.title || ''} ${doctor.firstName} ${doctor.lastName}`"
      />
      <img
        v-else
        src="/img/doc-placeholder.png"
        :alt="`تصویر ${doctor.title || ''} ${doctor.firstName} ${doctor.lastName}`"
      />
    </nuxt-link>
    <div class="name">
      <h3>
        <nuxt-link
          :to="`/doctors/psychology/${doctor.subscriberNumber}`"
          class="doctor-name"
        >{{doctor.title}} {{doctor.firstName}} {{doctor.lastName}}</nuxt-link>
      </h3>
      <p class="doctor-speciality">
        <strong>{{doctor.specialty.title}}</strong>
      </p>
      <div class="doctor-tags">
        <p>
          <span v-for="(tag,index) in doctor.custom_tags.slice(0,3)" :key="tag.id">
            {{tag.title}}
            <template v-if="index != 2">،</template>
          </span>
        </p>
        <div class="success-call hide-md-and-up">
          <Favorite />
          <span>{{doctor.success_call | persianDigit}}+</span>
        </div>
      </div>
    </div>
    <div class="price">
      <div class="success-call hide-md">
        <span>{{doctor.success_call | persianDigit}}+</span>
        جلسه رضایت بخش
      </div>
      <div>
        <div class="price-per-minute">{{1250 | persianDigit}} تومان / دقیقه</div>
        <v-btn :to="`/doctors/psychology/${doctor.subscriberNumber}`" class="select-btn" dark round>
          <span>انتخاب مشاور</span>
        </v-btn>
      </div>
    </div>
  </section>
</template>
<script>
import Available from "@/assets/svg/Available.svg?inline";
import NotAvailable from "@/assets/svg/NotAvailable.svg?inline";
import Favorite from "@/assets/svg/favorites_button.svg?inline";
export default {
  props: {
    doctor: {}
  },
  components: { Available, NotAvailable, Favorite }
};
</script>