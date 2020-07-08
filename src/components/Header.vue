<template>
  <section class="header">
    <div class="wrapper">
      <div class="header__topline">
        <div class="header__topline-logo">
          <div>D</div>
        </div>
        <div class="header__topline-brand">
          Daisy
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="less">
.header {
  width: 100%;
  height: 100vh;
  margin: 0;
  background-image: url('../assets/images/header.png');
  background-repeat: no-repeat;
  background-size: 100% 99.9%;
  &__topline {
    display: flex;
    padding-top: 50px;
    &-logo {
      .hexogonlogo(#fc635e, #0c252d, 59px, 68px);
    }
    &-brand {
      font-size: 25px;
      letter-spacing: 0px;
      line-height: 16px;
      color: #ffffff;
      font-weight: bold;
      font-family: "Gotham Pro";
      margin-left: 20px;
      margin-top: 10px;
    }
  }
}
</style>
