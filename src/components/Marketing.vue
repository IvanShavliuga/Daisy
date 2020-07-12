<template>
  <section class="landing">
    <div class="wrapper">
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
          <img class="landing__images-marketing" alt="marketing" src="../assets/images/marketing.png"/>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: 'Marketing'
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
    padding-top: 100px;
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
    &-marketing {
      top: 20px;
      left: -160px;
      z-index: 10;
    }
  }
}
</style>
