<template>
  <section class="clients">
    <div class="wrapper">
      <div class="clients__hexogon">
        <img class="clients__hexogon-image" src="../assets/images/quote.svg">
        <div class="clients__hexogon-border">
          <div></div>
          <div></div>
          <div></div>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: 'Clients'
}
</script>
<style lang="less">
.clients {
  width: 100%;
  height: 100vh;
  margin: 0;
  padding-top: 80px;
  padding-bottom: -40px;
  &__hexogon {
    .hexogonicon(@itemactive, 74px, 86px);
    text-align: center;
    margin-left: 45%;
    &-border {
      z-index: 40;
      position: absolute;
      top: -20px;
      left: 0;
      .hexogonborder(lighten(@itemactive, 12%), 4px, 74px, 86px);
    }
  }
}
</style>
