<style lang="scss" scoped>
section {
  border: 2px solid #1ad1c2;
  display: flex;
  align-items: center;
  margin: 20px 0;
  height: 150px;
  border-radius: 20px;
  justify-content: space-between;
  padding: 0 30px;
  @include media(sm) {
    flex-direction: column;
    height: auto;
  }
}
.step {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  position: relative;
  flex: 0 0 200px;
  height: 100%;
  @include media(sm) {
    flex: auto;
  }
  .label {
    position: absolute;
    top: 10px;
    right: 30px;
    width: 25px;
    height: 25px;
    border: 2px solid #43e7a5;
    color: #43e7a5;
    border-radius: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 16px;
    @include media(sm) {
      display: none;
    }
  }
  span {
    color: #9f9f9f;
    font-size: 14px;
    font-weight: normal;
    margin-bottom: 16px;
  }
  .image {
    height: 100px;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  img {
    max-height: 70px;
  }
}

.chevron {
  svg {
    width: 30px;
    height: 30px;
    @include media(sm) {
      transform: rotate(270deg);
    }
    path {
      fill: #43e7a5;
    }
  }
}
</style>
<template>
  <section>
    <div class="step">
      <div class="label">۱</div>
      <div class="image">
        <img src="~assets/img/doctor.png" />
      </div>
      <span>پزشک خود را از لیست انتخاب کنید</span>
    </div>
    <div class="chevron">
      <chevron />
    </div>
    <div class="step">
      <div class="label">۲</div>
      <div class="image">
        <img src="~assets/img/smartphone.png" />
      </div>
      <span>شماره موبایل خود را وارد کنید</span>
    </div>
    <div class="chevron">
      <chevron />
    </div>
    <div class="step">
      <div class="label">۳</div>
      <div class="image">
        <img src="~assets/img/money.png" />
      </div>
      <span>هزینه مشاوره خود را پرداخت کنید</span>
    </div>
    <div class="chevron">
      <chevron />
    </div>
    <div class="step">
      <div class="label">۴</div>
      <div class="image">
        <img src="~assets/img/call.png" />
      </div>
      <span>با پزشک تماس بگیرید</span>
    </div>
  </section>
</template>
<script>
import chevron from "@/assets/svg/chevron_left.svg?inline";
export default {
  components: {
    chevron
  }
};
</script>