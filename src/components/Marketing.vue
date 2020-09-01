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
            <source media="(max-width: 740px)" srcset="../assets/images/marketing_m.png 740w, ../assets/images/marketing_m1.png 560w"/>
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
  margin: 0;
  padding-top: 10px;
  padding-bottom: 40px;
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
  }
}
</style>
