<template>
  <section class="header">
    <div class="wrapper">
      <div class="header__topline">
        <div class="header__topline-leftblock">
          <div class="header__topline-logo">
            <div>D</div>
          </div>
          <div class="header__topline-brand">
            Daisy
          </div>
        </div>
        <nav class="header__topline-menu">
          <ul class="header__topline-list">
            <li class="header__topline-item">about</li>
            <li class="header__topline-item">portfolio</li>
            <li class="header__topline-item">services</li>
            <li class="header__topline-item">contact</li>
          </ul>
        </nav>
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
    justify-content: space-between;
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
    &-leftblock {
      display: flex;
      flex-grow: 1;
    }
    &-menu {
      flex-grow: 1;
    }
    &-list {
      display: flex;
      justify-content: flex-end;
    }
    &-item {
      list-style: none;
      text-transform: uppercase;
      margin: -15px 45px 0 0;
      color: #fff;
      font-size: 16px;
      letter-spacing: 1px;
      line-height: 36px;
      font-family: "P FEncore Sans Pro";
    }
  }
}
</style>
