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
            <source media="(max-width: 740px)" srcset="../assets/images/landing_m.png">
            <img class="landing__images-img" alt="advertising macbook" src="../assets/images/landing.png"/>
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
    img {
      margin-left: -150px;
      @media screen and (max-width: 1111px) {
        margin-left: -100px;
      }
      @media screen and (max-width: 890px) {
        margin-left: 0;
      }
    }
    @media screen and (max-width: @largetablet) {
      width: 100%;
      text-align: center;
    }
    &-img {
    }
  }
}
</style>
