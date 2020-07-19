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
          <picture>
            <source media="(max-width: 1115px)" srcset="../assets/images/macbook_m.png">
            <img class="landing__images-macbook" alt="advertising macbook" src="../assets/images/macbook.png"/>
          </picture>
          <picture>
            <source media="(max-width: 1115px)" srcset="../assets/images/desktop_m.png">
            <img class="landing__images-desktop" alt="advertising macbook" src="../assets/images/desktop.png"/>
          </picture>
          <picture>
            <source media="(max-width: 1115px)" srcset="../assets/images/tablet_m.png">
            <img class="landing__images-tablet" alt="advertising macbook" src="../assets/images/tablet.png"/>
          </picture>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: 'Landing'
}
</script>
<style lang="less">
.landing {
  width: 100%;
  height: 608px;
  margin: 0;
  padding-top: 30px;
  padding-bottom: 30px;
  background-color: @bodygraybg;
  .headersection();
  &__block {
    display: flex;
    justify-content: space-between;
    padding-top: 50px;
    width: 90%;
  }
  .textleftsection();
  &__title {
    width: 240px;
    margin: 0 auto;
  }
  &__images {
    width: 40%;
    position: relative;
    @media screen and (max-width: @largetablet) {
      width: 30%;
    }
    img {
      position: absolute;
    }
    &-desktop {
      top: 20px;
      left: -80px;
      z-index: 10;
      @media screen and (max-width: @largetablet) {
        left: -190px;
      }
    }
    &-macbook{
      top: 170px;
      left: -170px;
      z-index: 20;
      @media screen and (max-width: @largetablet) {
        left: -280px;
      }
    }
    &-tablet {
      top: 150px;
      left: 210px;
      z-index: 20;
      @media screen and (max-width: @largetablet) {
        left: 100px;
      }
    }
  }
}
</style>
