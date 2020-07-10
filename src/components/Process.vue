<template>
  <section class="process">
    <div class="wrapper">
      <h2 class="process__title">
        Our
        <span class="process__title-lastword">process</span>
      </h2>
      <p class="process__desc">Daisy is sagittis sem nibh id elit. Duis sed odio sit amet nibh
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
  width: 100%;
  height: 100vh;
  margin: 0;
  padding-top: 40px;
  &__title {
    width: 190px;
    margin: 0 auto;
    font-size: 28px;
    letter-spacing: 0px;
    line-height: 26px;
    color: @bodycolor;
    font-weight: 500;
    font-family: @bodyfont;
    text-align: center;
    text-transform: uppercase;
    padding-bottom: 10px;
    border-bottom: 1px solid #adadad;
    &-lastword {
      color: @itemactive;
    }
  }
  &__desc {
    font-family: @bodyfont;
    height: 51px;
    font-size: 20px;
    letter-spacing: 0px;
    line-height: 26px;
    color: @paragraphcolor;
    font-weight: 300;
    font-family: @bodyfont;
    text-align: center;
    width: 490px;
    margin: 20px auto;
  }
  &__steps {
    position: relative;
  }
  &__step1, &__step2, &__step3 {
    position: absolute;
    .hexogontext(@itemactive, @paragraphcolor, 174px, 201px);
  }
  &__step1 {
    left: 5px;
    top: 102px;
    z-index: 20;
  }
  &__step2 {
    left: 260px;
    top: 147px;
    z-index: 20;
  }
  &__step3 {
    left: 348px;
    top: -3px;
    z-index: 20;
  }
  &__photo {
    position: absolute;
    top: 241px;
    left: 49px;
    background-image: url('../assets/images/steps.png');
    .hexogonimage(white, 262px, 302px);
  }
}
</style>
