<template>
  <section class="landing">
    <div class="wrapper">
      <h2 class="landing__title">
        What do
        <span class="landing__title-lastword">we do?</span>
      </h2>
      <div class="landing__block">
        <div class="landing__text">
          <h3 class="landing__text-title">Landing page
          </h3>
          <p class="landing__text-desc">Daisy is sagittis sem nibh id elit. Duis sed odio sit amet nibh
            Daisy is sagittis sem nibh id elit. Duis sed odio sit amet nibh
            Daisy is sagittis sem nibh id elit. Duis sed odio sit amet nibh
            Daisy is sagittis sem nibh id elit. Duis sed odio sit amet nibh
          </p>
          <button class="landing__text-button">More details</button>
        </div>
        <div class="landing__images">
          <img class="landing__images-desktop" alt="landing desktop" src="../assets/images/desktop.png"/>
          <img class="landing__images-macbook" alt="landing macbook" src="../assets/images/macbook.png"/>
          <img class="landing__images-tablet" alt="landing tablet" src="../assets/images/tablet.png"/>
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
.landing {
  width: 100%;
  height: 100vh - 20px;
  margin: 0;
  padding-top: 40px;
  background-color: @bodygraybg;
  .headersection();
  &__block {
    display: flex;
    justify-content: space-between;
    padding-top: 50px;
  }
  .textleftsection();
  &__title {
    width: 240px;
    margin: 0 auto;
  }
  &__images {
    width: 40%;
    position: relative;
    img {
      position: absolute;
    }
    &-desktop {
      top: 20px;
      left: -80px;
      z-index: 10;
    }
    &-macbook{
      top: 170px;
      left: -170px;
      z-index: 20;
    }
    &-tablet {
      top: 150px;
      left: 210px;
      z-index: 20;
    }
  }
}
</style>
