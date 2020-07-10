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
              <h4 class="receive__block-title">clients</h4>
              <p class="receive__block-desc">Daisy is sagittis sem nibh id elit. Duis sed odio sit amet nibh</p>
            </div>
          </li>
          <li class="receive__block-item">
            <div class="receive__block-hexogon">
              <img class="receive__block-image" src="../assets/images/brand2.svg">
              <h4 class="receive__block-title">brands</h4>
              <p class="receive__block-desc">Daisy is sagittis sem nibh id elit. Duis sed odio sit amet nibh</p>
            </div>
          </li>
          <li class="receive__block-item">
            <div class="receive__block-hexogon">
              <img class="receive__block-image" src="../assets/images/brand3.svg">
              <h4 class="receive__block-title">marketing</h4>
              <p class="receive__block-desc">Daisy is sagittis sem nibh id elit. Duis sed odio sit amet nibh</p>
            </div>
          </li>
          <li class="receive__block-item">
            <div class="receive__block-hexogon">
              <img class="receive__block-image" src="../assets/images/brand4.svg">
              <h4 class="receive__block-title">adv.</h4>
              <p class="receive__block-desc">Daisy is sagittis sem nibh id elit. Duis sed odio sit amet nibh</p>
            </div>
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>
<style lang="less">
.receive {
  width: 100%;
  height: 80vh;
  margin: 0;
  padding-top: 40px;
  &__title {
    width: 353px;
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
  &__subtitle {
    font-family: @bodyfont;
    height: 51px;
    font-size: 20px;
    letter-spacing: 0px;
    line-height: 26px;
    color: @paragraphcolor;
    font-weight: 300;
    font-family: "P FEncore Sans Pro";
    text-align: center;
    width: 490px;
    margin: 20px auto;
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
      .hexogonimage(@itemactive, 100px, 116px);
      text-align: center;
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
