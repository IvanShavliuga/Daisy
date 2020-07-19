<template>
  <section class="receive">
    <div class="wrapper">
      <h2 class="receive__title">
        What can
        <span class="receive__title-lastword">you receive?</span>
      </h2>
      <h3 class="receive__subtitle">
        Daisy is sagittis sem nibh id elit. Duis sed odio sit amet nibh
        Daisy is sagittis sem nibh id elit. Duis sed odio sit amet nibh
      </h3>
      <div class="receive__block">
        <ul class="receive__block-list">
          <li class="receive__block-item">
            <div class="receive__block-hexogon">
              <img class="receive__block-image" src="../assets/images/brand1.svg">
              <div class="receive__block-border">
                <div></div>
                <div></div>
                <div></div>
              </div>
            </div>
            <h4 class="receive__block-title">clients</h4>
            <p class="receive__block-desc">Daisy is sagittis sem nibh id elit. Duis sed odio sit amet nibh</p>
          </li>
          <li class="receive__block-item">
            <div class="receive__block-hexogon">
              <img class="receive__block-image" src="../assets/images/brand2.svg">
              <div class="receive__block-border">
                <div></div>
                <div></div>
                <div></div>
              </div>
            </div>
            <h4 class="receive__block-title">brands</h4>
            <p class="receive__block-desc">Daisy is sagittis sem nibh id elit. Duis sed odio sit amet nibh</p>
          </li>
          <li class="receive__block-item">
            <div class="receive__block-hexogon">
              <img class="receive__block-image" src="../assets/images/brand3.svg">
              <div class="receive__block-border">
                <div></div>
                <div></div>
                <div></div>
              </div>
            </div>
            <h4 class="receive__block-title">marketing</h4>
            <p class="receive__block-desc">Daisy is sagittis sem nibh id elit. Duis sed odio sit amet nibh</p>
          </li>
          <li class="receive__block-item">
            <div class="receive__block-hexogon">
              <img class="receive__block-image" src="../assets/images/brand4.svg">
              <div class="receive__block-border">
                <div></div>
                <div></div>
                <div></div>
              </div>
            </div>
            <h4 class="receive__block-title">adv.</h4>
            <p class="receive__block-desc">Daisy is sagittis sem nibh id elit. Duis sed odio sit amet nibh</p>
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: 'Receive'
}
</script>
<style lang="less">
.receive {
  height: 576px;
  margin: 0;
  padding-top: 40px;
  .headersection();
  &__title {
    width: 360px;
    margin: 0 auto;
  }
  &__block {
    margin-top: 100px;
    &-list {
      display: flex;
      justify-content: space-between;
    }
    &-item {
      margin: 0 10px;
      list-style: none;
      width: 130px;
      text-align: center;
    }
    &-hexogon {
      .hexogonicon(@itemactive, 100px, 116px);
      text-align: center;
    }
    &-border {
      z-index: 20;
      position: absolute;
      top: -30px;
      left: 0;
      .hexogonborder(lighten(@itemactive, 12%), 4px, 100px, 116px);
    }
    &-title {
      position: relative;
      text-transform: uppercase;
      margin-top: 60px;
      font-size: 20px;
      letter-spacing: 0px;
      line-height: 20px;
      font-weight: 500;
      font-family: @bodyfont;
      text-align: center;
      color: @bodycolor;
      &:after {
        position: absolute;
        content: ' ';
        width: 57px;
        height: 1px;
        background-color: @paragraphcolor;
        top: 30px;
        left: 23%;
      }
    }
    &-desc {
      font-size: 15px;
      letter-spacing: 0px;
      line-height: 18px;
      color: @paragraphcolor;
      font-weight: 300;
      font-family: @bodyfont;
      text-align: center;
      width: 130px;
    }
  }
}

</style>
