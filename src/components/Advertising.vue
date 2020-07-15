<template>
  <section class="advertising">
    <div class="wrapper">
      <div class="advertising__block">
        <div class="advertising__images">
          <img class="advertising__images-macbook" alt="advertising macbook" src="../assets/images/macbook2.png"/>
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
  height: 90vh;
  margin: 0;
  padding-top: 40px;
  padding-bottom: -40px;
  background-color: #fff;
  &__block {
    display: flex;
    justify-content: space-between;
    padding-top: 100px;
  }
  .textleftsection();
  &__text {
    text-align: right;
    &-desc {
      text-align: right;
    }
    &-title {
      margin-right: 25px;
      text-align: right;
      &:before {
        left: 400px;
      }
    }
  }
  &__images {
    width: 40%;
    position: relative;
    img {
      position: absolute;
    }
    &-macbook{
      top: 10px;
      right: -80px;
      z-index: 20;
    }
  }
}
</style>
