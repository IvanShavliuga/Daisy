<template>
<section class="footer">
  <div class="footer__map">
  </div>
  <div class="footer__bottom">
    <div class="footer__bottom-logoblock">
      <div class="footer__bottom-logo">
        <div>D</div>
      </div>
      <div class="footer__bottom-brand">
        Daisy
      </div>
    </div>
  </div>
</section>
</template>
<style lang="less">
.footer {
  width: 100%;
  height: 338px + 208px;
  padding-top: 150px;
  &__map {
    background-image: url(../assets/images/map.png);
    background-repeat: no-repeat;
    height: 338px;
  }
  &__bottom {
    position: relative;
    background-image: url(../assets/images/footer.png);
    height: 208px;
    background-repeat: no-repeat;
    background-position: center center;
    background-size: 100%;
    &-logo {
      font-family: @logofont;
      .hexogonlogo(@logocolor, #0c252d, 59px , 68px);
    }
    &-brand {
      font-size: 35px;
      letter-spacing: 0px;
      line-height: 16px;
      color: #ffffff;
      font-weight: bold;
      font-family: @logofont;
      margin-left: 20px;
      margin-top: 5px;
    }
    &-logoblock {
      display: flex;
      flex-grow: 1;
      position: absolute;
      left: 50%;
      top: 50%;
      transform: translate(-50%, -50%);
    }
  }
}
</style>
