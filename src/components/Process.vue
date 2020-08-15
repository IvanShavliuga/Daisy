<template>
  <section class="process">
    <div class="wrapper">
      <h2 class="process__title">
        Our
        <span class="process__title-lastword">process</span>
      </h2>
      <p class="process__subtitle">Daisy is sagittis sem nibh id elit. Duis sed odio sit amet nibh
        Daisy is sagittis sem nibh id elit. Duis sed odio sit amet nibh
      </p>
      <div class="process__steps">
        <div class="process__step1">
          <div></div>
          <div>
            <h4>Step
              <span>1</span>
            </h4>
            <p>This is Photoshop's version  of loren ipsumm. Proin</p>
            <i class="process__steps-img">
              <img class="process__step1-img" src="../assets/images/step1.svg">
            </i>
          </div>
          <div></div>
        </div>
        <div class="process__step2">
          <div></div>
          <div>
            <h4>Step
              <span>2</span>
            </h4>
            <p>This is Photoshop's version  of loren ipsumm. Proin</p>
            <i class="process__steps-img">
              <img class="process__step2-img" src="../assets/images/step2.svg">
            </i>
          </div>
          <div></div>
        </div>
        <div class="process__step3">
          <div></div>
          <div>
            <h4>Step
              <span>3</span>
            </h4>
            <p>This is Photoshop's version  of loren ipsumm. Proin</p>
            <i class="process__steps-img">
              <img class="process__step3-img" src="../assets/images/step3.svg">
            </i>
          </div>
          <div></div>
        </div>
        <div class="process__step4">
          <div></div>
          <div>
            <h4>Step
              <span>4</span>
            </h4>
            <p>This is Photoshop's version  of loren ipsumm. Proin</p>
            <i class="process__steps-img stepimg4">
              <img class="process__step4-img" src="../assets/images/step4.svg">
            </i>
            <i class="process__steps-img">
              <img class="process__step4-img" src="../assets/images/step5.svg">
            </i>
          </div>
          <div></div>
        </div>
        <div class="process__photo">
          <div></div>
          <div></div>
          <div></div>
          <div></div>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: 'Process'
}
</script>
<style lang="less">
.process {
  height: 841px;
  margin: 0;
  padding-top: 40px;
  @media screen  and (max-width: @desktop) {
    height: 741px;
  }
  @media screen  and (max-width: 599px) {
    height: 841px;
  }
  @media screen and (max-width: 695px) {
    height: 920px;
  }
  .headersection();
  &__title {
    width: 190px;
    margin: 0 auto;
  }
  &__steps {
    position: relative;
    width: 70%;
    margin: 30px auto;
    @media screen and (min-width: @tablet) and (max-width: @desktop) {
      transform: scale(0.8);
      margin-left: 10px;
      margin-right: 0;
    }
    @media screen and (min-width: @largephone) and (max-width: @tablet) {
      transform: scale(0.75);
      margin: 50px 2%;
    }
    @media screen and (min-width: @phone) and (max-width: @largephone) {
      transform: scale(0.8);
      margin: 110px 0 10px -10px;
    }
    &-img {
      position: absolute;
      top: -15px;
      left: -15px;
      z-index: 50;
      background-color: @stepsline;
      border-radius: 50%;
      width: 34px;
      height: 32px;
      display: block;
      padding-top: 4px;
    }
  }
  &__step1, &__step2, &__step3 {
    position: absolute;
    .hexogontext(@paragraphcolor, 174px, 201px);
  }
  &__step1 {
    left: 2px;
    top: 101px;
    z-index: 20;
    @media screen  and (min-width: @tablet) {
      left: 7px;
    }
    @media screen and (max-width: 696px) {
      top: -38px;
      left: 166px;
    }
    @media screen and (max-width: 520px) {
      left: 85px;
    }
    div:last-child:before {
      @media screen and (min-width: 696px) {
        display: none;
      }
    }
    div:first-child:after, div:first-child:before {
      height: 4px;
      background-color: @stepsline;
      width: 201px / 2 ;
    }
    div:nth-child(2):before {
      content: ' ';
      position: absolute;
      top: 47px;
      left: 123px;
      background-color: @stepsline;
      width: 97px;
      height: 4px;
      z-index: 30;
      transform: rotateZ(90deg);
      @media screen and (min-width: 696px) and (max-width: @tablet) {
        display: none;
      }
    }
  }
  &__step2 {
    left: 260px;
    top: 147px;
    @media screen and (max-width: 695px) {
      top: 100px;
      left: 276px;
    }
    @media screen and (min-width: 696px) and (max-width: @tablet) {
      left: 177px;
      top: 97px;
    }
    @media screen and (max-width: 520px) {
      left: 183px;
      top: 107px;
    }
    z-index: 20;
    i:last-child {
      @media screen and (max-width: 695px) {
        top: -68px;
        left: 52px;
      }
    }
    div:nth-child(2):after {
      @media screen and (min-width: @tablet) {
        content: ' ';
        position: absolute;
        top: 49px;
        left: -51px;
        background-color: @stepsline;
        width: 101px;
        height: 4px;
        z-index: 30;
        transform: rotateZ(90deg);
      }
      @media screen and (min-width: 696px) and (max-width: @tablet) {
        display: none;
      }
    }
    div:nth-child(2):after {
      @media screen and (max-width: 695px) {
        content: ' ';
        position: absolute;
        top: 50px;
        right: -51px;
        background-color: @stepsline;
        width: 103px;
        height: 4px;
        z-index: 30;
        transform: rotateZ(90deg);
      }
    }
    div:first-child:before {
      @media screen and (max-width: 695px) {
        height: 4px;
        background-color: @stepsline;
        width: 208px / 2 ;
      }
    }
    div:first-child:after {
      @media screen and (min-width: 696px) {
        height: 4px;
        background-color: @stepsline;
        width: 208px / 2 ;
        z-index: 20;
      }
    }
    div:last-child:before {
      @media screen and (max-width: 695px) {
        height: 4px;
        background-color: @stepsline;
        width: 201px / 2.5 ;
        top: 20px;
        z-index: 20;
      }
    }
  }
  &__step3 {
    left: 348px;
    top: -3px;
    z-index: 20;
    @media screen and (max-width: 695px) {
      top: 280px;
      left: 240px;
    }
    @media screen and (min-width: 696px) and (max-width: @tablet) {
      left: 265px;
      top: -54px;
    }
    @media screen and (max-width: 520px) {
      left: 153px;
      top: 294px;
    }
    i:last-child {
      z-index: 50;
      @media screen and (max-width: 695px) {
        top: -48px;
        left: 112px;
      }
    }
    div:first-child:after, div:first-child:before {
      @media screen and (min-width: 696px) {
        height: 4px;
        background-color: @stepsline;
        width: 201px / 2 ;
      }
    }
    div:first-child:before {
      @media screen  and (max-width: 695px) {
        height: 4px;
        background-color: @stepsline;
        width: 201px / 4.8 ;
        right: -5px;
        top: 40px;
        z-index: 20;
      }
    }
    div:nth-child(2):after {
      @media screen and (min-width: 696px) {
        content: ' ';
        position: absolute;
        top: 49px;
        left: -51px;
        background-color: @stepsline;
        width: 104px;
        height: 4px;
        z-index: 30;
        transform: rotateZ(90deg);
      }
    }
    div:nth-child(2):before {
      content: ' ';
      position: absolute;
      top: 50px;
      right: -51px;
      background-color: @stepsline;
      width: 103px;
      height: 4px;
      z-index: 30;
      transform: rotateZ(90deg);
    }
    div:last-child:before {
      @media screen and (max-width: 695px) {
        height: 4px;
        background-color: @stepsline;
        width: 201px / 2 ;
      }
    }
    div:last-child:after {
      @media screen and (min-width: 520px)  and (max-width: 695px) {
        height: 4px;
        background-color: @stepsline;
        width: 201px / 2.8 ;
        left: 22px;
        top: 30px;
        z-index: 20;
      }
    }
  }
  &__step4 {
    position: absolute;
    .hexogontext(@paragraphcolor, 262px, 302px);
    left: 348px + 174px;
    top: 70px;
    z-index: 20;
    @media screen and (min-width: 696px) and (max-width: @tablet) {
      left: 348px + 90px - 87px;
      top: 70px;
    }
    @media screen and (min-width: @tablet) and (max-width: 831px) {
      left: 348px + 174px - 87px;
      top: 70px + 53px;
    }
    @media screen and (max-width: 695px) {
      top: 367px;
      left: -8px;
    }
    @media screen and (max-width: 520px) {
      top: 423px;
      left: -16px;
    }
    i:last-child {
      top: 200px;
      left: 110px;
      padding-top: 6px;
      height: 28px;
      background-color: white;
      border: 3px solid @stepsline;
    }
    div:first-child:after, div:first-child:before {
      @media screen and (min-width: 696px) {
        height: 4px;
        background-color: @stepsline;
        width: 262px / 1.7;
      }
    }
    div:first-child:after {
      top: 302px / 9 + 3px;
      left: -11px;
      @media screen and (max-width: 831px)  {
        left: 80px;
        top: 10px;
        width: 55px;
      }
      @media screen and (max-width: 695px) {
        top: 302px / 9 + 3px;
        left: -11px;
        width: 262px / 1.7;
      }
    }
    div:first-child:before {
      top: 302px / 9  + 3px;
      right: -11px;
    }
    div:nth-child(2) {
      h4 {
        top: -55px;
        left: 95px;
      }
      p {
        top: 10px;
        left: 60px;
      }
      .stepimg4 {
        @media screen and (max-width: 831px)  {
          left: 70px;
          top: -70px;
        }
        @media screen and (max-width: 695px) {
          top: -13px;
          left: 245px;
        }
      }
    }
    div:nth-child(2):before {
      content: ' ';
      position: absolute;
      top: 75px;
      right: -75px;
      background-color: @stepsline;
      width: 151px;
      height: 4px;
      z-index: 30;
      transform: rotateZ(90deg);
    }
    div:last-child:after {
      top: 302px / 9 + 4px;
      left: -10px;
    }
    div:last-child:before {
      top: 302px / 9  + 4px;
      right: -10px;
      background-color: @stepsline;
      height: 4px;
      z-index: 30;
    }
  }
  &__step1, &__step2, &__step {
    z-index: 30;
  }
  &__photo {
    position: absolute;
    top: 239px;
    left: 47px;
    z-index:1;
    background-image: url('../assets/images/steps.jpg');
    .hexogonimage(white, 262px, 302px);
    @media screen and (max-width: 520px) {
      display: none;
    }
    @media screen and (max-width: 695px) {
      top: 90px;
      left: 17px;
    }
    &:after {
      content: ' ';
      position: absolute;
      top: 31px;
      left: 125px;
      background-color: @stepsline;
      width: 94px;
      height: 4px;
      z-index: 30;
      transform: rotateZ(30.3deg);
      @media screen and (min-width: @phone) and (max-width: @tablet) {
        display: none;
      }
    }
  }
}
</style>
