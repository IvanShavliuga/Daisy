<template>
  <section class="receive">
    <div class="wrapper">
      <h2 class="receive__title">
        What can
        <span class="receive__title-lastword">you receive?</span>
      </h2>
      <h3 class="receive__subtitle">
        Daisy is sagittis sem nibh id elit. Duis sed odio sit amet nibh
      </h3>
    </div>
  </section>
</template>
<style lang="less">
.receive {
  &__title {
    font-size: 28px;
    letter-spacing: 0px;
    line-height: 26px;
    color: @bodycolor;
    font-weight: 500;
    font-family: @bodyfont;
    text-align: center;
    text-transform: uppercase;
    &-lastword {
      color: @itemactive;
    }
  }
  &__subtitle {
    font-family: @bodyfont;
    height: 51px;
    font-size: 20px;
    letter-spacing: 0px;
    line-height: 26px;
    color: #adadad;
    font-weight: 300;
    font-family: "P FEncore Sans Pro";
    text-align: center;
  }
}

</style>
