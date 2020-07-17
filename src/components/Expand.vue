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
  width: 100% -40px;
  height: 100% -160px;
  margin: 0;
  background-image: url('../assets/images/expand.jpg');
  background-repeat: no-repeat;
  background-size: 100% 99.9%;
  padding: 80px 20px 80px 20px;
  &__block {
    border: 8px solid rgba(99, 99, 99, 0.4);
    height: 75vh;
    width: 95%;
    text-align: center;
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
      margin-top: 15px;
      .buttontransparent();
    }
  }
}
</style>
