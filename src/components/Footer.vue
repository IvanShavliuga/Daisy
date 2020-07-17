<template>
<section class="footer">
  <div class="footer__map">
    <div class="footer__hexogon">
      <div class="footer__hexogon-first"></div>
      <div class="footer__hexogon-info">
        <h4 class="footer__hexogon-title">Daisy</h4>
        <p class="footer__hexogon-text">615 4th Ave S, Jacksonville Beach, FL 32250</p>
      </div>
      <div class="footer__hexogon-last"></div>
      <div class="footer__hexogon-border">
        <div></div>
        <div></div>
        <div></div>
      </div>
    </div>
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
    position: relative;
    background-image: url(../assets/images/map.jpg);
    background-repeat: no-repeat;
    height: 338px;
  }
  &__hexogon {
    position: absolute;
    left: 50%;
    top: -20%;
    transform: translate(-50%, 20%);
    z-index: 20;
    width: 209px;
    height: 242px;
    background-color: @itemactive;
    .hexogonicon(@itemactive, 209px, 242px);
    &-border {
      z-index: 20;
      position: absolute;
      top: -60px;
      left: 0;
      .hexogonborder(lighten(@itemactive, 12%), 8px, 209px, 242px);
      div:first-child {
        &:after {
          top: 242px / 9 + 2px;
          left: -7px + 8px - 7px;
        }
        &:before {
          top: 242px / 9 + 2px;
          right: -7px + 8px - 7px;
        }
      }
      div:last-child {
        &:after {
          bottom: 242px / 9 + 3px;
          left: -7px + 8px - 7px;
        }
        &:before {
          bottom: 242px / 9 + 3px;
          right: -7px + 8px - 7px;
        }
      }
    }
    &:before {
      top: -59px;
    }
    &:after {
      bottom: -59px;
    }
    text-align: center;
    &-title {
      font-size: 27px;
      letter-spacing: 0px;
      color: #ffffff;
      font-weight: 500;
      font-family: @bodyfont;
      margin-bottom: 10px;
      margin-top: 10px;
    }
    &-text {
      font-size: 16px;
      letter-spacing: 0px;
      color: #ffffff;
      font-weight: 500;
      font-family: @bodyfont;
      margin-top: 10px;
    }
  }
  &__bottom {
    position: relative;
    background-image: url(../assets/images/footer.jpg);
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
