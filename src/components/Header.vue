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
            <li class="header__topline-item active">about</li>
            <li class="header__topline-item">portfolio</li>
            <li class="header__topline-item">services</li>
            <li class="header__topline-item">contact</li>
          </ul>
        </nav>
      </div>
      <div class="header__block">
        <h1 class="header__block-title">
          <span class="header__block-firstword">Clients</span>
          in your business
        </h1>
        <h2 class="header__block-subtitle">
          Your clients on the internet. Learn how to receive them.
        </h2>
        <div class="header__block-center">
          <button class="header__block-button">
            I want clients
          </button>
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
    justify-content: space-between;
    padding-top: 50px;
    &-logo {
      .hexogonlogo(@logocolor, #0c252d, 59px, 68px);
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
    .active {
      color: @itemactive;
      border-bottom: 3px solid @itemactive;
    }
  }
  &__block {
    height: 40vh;
    padding: 11% 15%;
    &-title {
      color: @headercolor;
      font-size: 51px;
      line-height: 36px;
      font-weight: bold;
      font-family: "P FEncore Sans Pro";
      text-transform: uppercase;
      word-spacing: 10px;
      position: relative;
      margin-bottom: 10px;
      &:after, &:before {
        content: ' ';
        position: absolute;
        display: block;
        width: 107px;
        height: 1px;
        background-color: #444;
        border: 4px solid #444;
      }
      &:after {
        top: 10px;
        left: -140px;
      }
      &:before {
        top: 10px;
        right: -120px;
      }
    }
    &-firstword {
      color: @headerfirstword;
    }
    &-subtitle {
      font-size: 24px;
      letter-spacing: 0px;
      line-height: 26px;
      color: @headercolor;
      font-family: "P FEncore Sans Pro";
      text-align: center;
      margin-top: 20px;
    }
    &-button {
      font-size: 24px;
      letter-spacing: 0px;
      line-height: 26px;
      color: @itemactive;
      font-weight: 300;
      font-family: "P FEncore Sans Pro";
      text-align: center;
      background: transparent;
      border: 2px solid @itemactive;
      width: 205px;
      height: 56px;
      border-radius: 7px;
    }
    &-center {
      margin-top: 40px;
      text-align: center;
    }
  }
}
</style>
