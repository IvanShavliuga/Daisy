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
      <div class="process__step1">
        <div></div>
        <div></div>
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
  &__photo {
    background-image: url('../assets/images/steps.png');
    .hexogonimage(white, 262px, 302px);
  }
  &__step1 {
    position: relative;
    //.hexogontext(red, 1px, 174px, 201px);
  }
}
</style>
