<template>
  <section class="marketing">
    <div class="wrapper">
      <div class="marketing__block">
        <div class="marketing__text">
          <h3 class="marketing__text-title">Marketing
          </h3>
          <p class="marketing__text-desc">Daisy is sagittis sem nibh id elit. Duis sed odio sit amet nibh
            Daisy is sagittis sem nibh id elit. Duis sed odio sit amet nibh
            Daisy is sagittis sem nibh id elit. Duis sed odio sit amet nibh
            Daisy is sagittis sem nibh id elit. Duis sed odio sit amet nibh
          </p>
          <button class="marketing__text-button">More details</button>
        </div>
        <div class="marketing__images">
          <picture>
            <source media="(max-width: 1115px)" srcset="../assets/images/marketing_m.png">
            <img class="marketing__images-marketing" alt="marketing" src="../assets/images/marketing.png"/>
          </picture>
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
<style scoped lang="less">
.marketing {
  width: 100%;
  height: 533px;
  margin: 0;
  padding-top: 10px;
  padding-bottom: -40px;
  background-color: @bodygraybg;
  .headersection();
  &__block {
    display: flex;
    justify-content: space-between;
    padding-top: 100px;
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
    &-marketing {
      top: 20px;
      left: -160px;
      z-index: 10;
      @media screen and (max-width: @largetablet) {
        left: -260px;
      }
    }
  }
}
</style>
