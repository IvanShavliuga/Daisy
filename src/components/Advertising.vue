<template>
  <section class="advertising">
    <div class="wrapper">
      <div class="advertising__block">
        <div class="advertising__images">
          <picture>
            <source media="(max-width: 500px)" srcset="../assets/images/macbook2_mobile.png">
            <img class="advertising__images-macbook" alt="advertising macbook" src="../assets/images/macbook2.png"/>
          </picture>
        </div>
        <div class="advertising__text">
          <h3 class="advertising__text-title">Advertising
          </h3>
          <p class="advertising__text-desc">Daisy is sagittis sem nibh id elit. Duis sed odio sit amet nibh
            Daisy is sagittis sem nibh id elit. Duis sed odio sit amet nibh
            Daisy is sagittis sem nibh id elit. Duis sed odio sit amet nibh
            Daisy is sagittis sem nibh id elit. Duis sed odio sit amet nibh
          </p>
          <button class="advertising__text-button">More details</button>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: 'Advertising'
}
</script>
<style lang="less">
.advertising {
  width: 100%;
  margin: 0;
  padding-top: 10px;
  padding-bottom: 40px;
  background-color: #fff;
  &__block {
    display: flex;
    justify-content: space-between;
    padding-top: 100px;
    width: 90%;
    @media screen and (max-width: @largetablet) {
      flex-direction: column!important;
      width: 100%;
    }
  }
  .textleftsection();
  &__text {
    text-align: right;
    @media screen and (max-width: @largetablet) {
      text-align: left!important;
    }
    &-desc {
      text-align: right;
      @media screen and (max-width: @largetablet) {
        text-align: left!important;
      }
    }
    &-title {
      margin-right: 25px;
      text-align: right;
      position: relative;
      @media screen and (max-width: @largetablet) {
        margin-left: 25px!important;
        margin-right: 0!important;
        text-align: left!important;
      }
      &:before {
        right: -30px;
        left: auto;
        @media screen and (max-width: @largetablet) {
          left: -30px;
          right: auto;
        }
      }
    }
  }
  &__images {
    width: 40%;
    @media screen and (max-width: @largetablet) {
      width: 100%;
      text-align: center;
    }
  }
}
</style>
