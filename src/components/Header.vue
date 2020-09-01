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
        <nav class="header__topline-menu" v-show="showmenu">
          <ul class="header__topline-list">
            <li class="header__topline-item active">about</li>
            <li class="header__topline-item">portfolio</li>
            <li class="header__topline-item">services</li>
            <li class="header__topline-item">contact</li>
          </ul>
        </nav>
        <!--<div class="header__topline-burger" @click="showmenu=!showmenu">
          <span></span>
          <span></span>
          <span></span>
        </div>-->
      </div>
      <div class="header__block">
        <h1 class="header__block-title">
          <span class="header__block-firstword">Clients</span>
          in your business
        </h1>
        <h3 class="header__block-subtitle">
          Your clients on the internet. Learn how to receive them.
        </h3>
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
  name: 'Header',
  data () {
    return {
      showmenu: true
    }
  }
}
</script>
<style scoped lang="less">
.header {
  height: 849px;
  margin: 0;
  background-image: url('../assets/images/header.jpg');
  background-repeat: no-repeat;
  background-size: 100% 99.9%;
  &__topline {
    display: flex;
    justify-content: space-between;
    padding-top: 45px;
    width: 90%;
    @media screen and (max-width: @tablet) {
      flex-direction: column;
      justify-content: center;
    }
    .logobrand();
    &-leftblock {
      display: flex;
      flex-grow: 1;
      @media screen and (max-width: 1120px) {
        padding-left: 40px;
      }
      @media screen and (max-width: @tablet) {
        justify-content: center;
      }
    }
    &-menu {
      flex-grow: 1;
      @media screen and (max-width: @tablet) {
        margin-top: 20px;
      }
    }
    &-list {
      display: flex;
      justify-content: flex-end;
      @media screen and (max-width: 520px) {
        flex-direction: column;
        justify-content: center;
      }
      @media screen and (max-width: @tablet) {
        justify-content: space-between;
      }
    }
    &-item {
      list-style: none;
      text-transform: uppercase;
      margin: -15px 25px 0 0;
      color: #fff;
      font-size: 16px;
      letter-spacing: 1px;
      line-height: 36px;
      font-family: @bodyfont;
      @media screen and (max-width: @tablet) {
        margin: 0 15px 5px -5px;
      }
    }
    .active {
      color: @itemactive;
      border-bottom: 3px solid @itemactive;
      @media screen and (max-width: 695px) {
        border-bottom: none;
        font-weight: bold;
      }
    }
  }
  &__block {
    height: 400px;
    &-title {
      .titlepicture();
      &:after, &:before {
        content: ' ';
        position: absolute;
        display: block;
        width: 107px;
        height: 1px;
        background-color: #444;
        border: 4px solid #444;
        @media screen and (max-width: @largetablet) {
          width: 50px;
        }
        @media screen and (max-width: 901px) {
          display: none;
        }
      }
      &:after {
        top: 25px;
        left: -140px;
        @media screen and (max-width: @largetablet) {
          left: -80px;
        }
      }
      &:before {
        top: 25px;
        right: -120px;
        @media screen and (max-width: @largetablet) {
          right: -60px;
        }
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
      font-family: @bodyfont;
      text-align: center;
      margin-top: 20px;
      @media screen and (max-width: 695px) {
        margin-top: 40px;
      }
      @media screen and (max-width: 500px) {
        font-size: 20px;
      }
    }
    &-button {
      .buttontransparent();
    }
    &-center {
      margin-top: 40px;
      text-align: center;
    }
  }
}
</style>
