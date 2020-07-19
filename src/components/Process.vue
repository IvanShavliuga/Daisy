<template>
  <section class="process">
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
  </section>
</template>
<script>
export default {
  name: 'Process'
}
</script>
<style lang="less">
.process {
  width: 100%;
  height: 841px;
  margin: 0;
  padding-top: 40px;
  .headersection();
  &__title {
    width: 190px;
    margin: 0 auto;
  }
  &__steps {
    position: relative;
    width: 90%;
    height: 700px;
    margin: 50px 0 50px auto;
    @media screen  and (min-width: @desktop) {
      margin-left: 70px;
    }
    @media screen and (max-width: @largetablet)  {
      margin: 5% 0 50px 7%;
    }
    &-img {
      position: absolute;
      top: -15px;
      left: -15px;
      z-index: 40;
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
    left: 5px;
    top: 101px;
    z-index: 20;
    div:nth-child(2) {
      border-right: none;
    }
    div:last-child:before {
      display: none;
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
    }
  }
  &__step2 {
    left: 260px;
    top: 147px;
    z-index: 20;
    i {
      padding-top: 8px;
      height: 28px;
    }
    div:nth-child(2):after {
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
    div:first-child:after {
      height: 4px;
      background-color: @stepsline;
      width: 208px / 2 ;
    }
  }
  &__step3 {
    left: 348px;
    top: -3px;
    z-index: 20;
    div:first-child:after, div:first-child:before {
      height: 4px;
      background-color: @stepsline;
      width: 201px / 2 ;
    }
    div:nth-child(2):after {
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
  }
  &__step4 {
    position: absolute;
    .hexogontext(@paragraphcolor, 262px, 302px);
    left: 348px + 174px;
    top: 70px;
    @media screen and (max-width: @largetablet)  {
      left: 348px + 174px - 87px;
      top: 70px + 53px;
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
      height: 4px;
      background-color: @stepsline;
      width: 262px / 1.7;
    }
    div:first-child:after {
      top: 302px / 9 + 3px;
      left: -11px;
      @media screen and (max-width: @largetablet)  {
        left: 80px;
        top: 10px;
        width: 55px;
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
        @media screen and (max-width: @largetablet)  {
          left: 70px;
          top: -70px;
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
  &__photo {
    position: absolute;
    top: 239px;
    left: 47px;
    background-image: url('../assets/images/steps.jpg');
    .hexogonimage(white, 262px, 302px);
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
    }
  }
}
</style>
