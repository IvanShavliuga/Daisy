<template>
<section class="expand">
  <div class="wrapper">
    <div class="expand__block">
      <h2 class="expand__block-title">
        <span class="expand__block-firstword">Expand</span>
        your business
      </h2>
      <button class="expand__block-button">
        Join us
      </button>
    </div>
  </div>
</section>
</template>
<style lang="less">
.expand {
  height: 606px;
  margin: 0;
  background-image: url('../assets/images/expand.jpg');
  background-repeat: no-repeat;
  background-size: 100% 99.9%;
  padding: 80px 20px;
  @media screen and (max-width: @largetablet) {
    height: 350px;
    padding: 80px 0;
  }
  &__block {
    border: 8px solid rgba(99, 99, 99, 0.4);
    height: 570px;
    text-align: center;
    @media screen and (max-width: @largetablet) {
      height: 300px;
    }
    &-title {
      font-size: 51px;
      letter-spacing: 0px;
      line-height: 18px;
      font-weight: bold;
      font-family: @bodyfont;
      text-align: center;
      color: #fff;
      .titlepicture();
      margin-top: 18%;
    }
    &-firstword {
      color: @itemactive;
    }
    &-button {
      margin-top: 35px;
      .buttontransparent();
    }
  }
}
</style>
