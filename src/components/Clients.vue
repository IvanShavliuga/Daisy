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
      <div class="clients__slider">
        <ul class="clients__slider-list">
          <li class="clients__slider-item">
            <p class="clients__slider-text">
              Daisy is sagittis sem nibh id elit. Duis sed odio sit amet nibh
              Daisy is sagittis sem nibh id elit. Duis sed odio sit amet nibh
            </p>
            <div class="clients__slider-photo">
              <img class="clients__slider-avatar" :src="avatar" :alt="avatar">
              <div class="clients__slider-first"></div>
              <div class="clients__slider-second"></div>
              <div class="clients__slider-third"></div>
              <div class="clients__slider-last"></div>
            </div>
            <div class="clients__slider-text">
              <h4 class="clients__slider-title">
                <span class="clients__slider-firstname">Alian</span>
                Richman
              </h4>
              <p class="clients__slider-prof">CEO of romantika</p>
            </div>
          </li>
        </ul>
        <div class="clients__slider-nav">
          <button class="clients__slider-prev"></button>
          <button class="clients__slider-next"></button>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
import client1 from '../assets/images/clients_1.png'
export default {
  name: 'Clients',
  data () {
    return {
      avatar: client1
    }
  }
}
</script>
<style lang="less">
.clients {
  height: 400px;
  margin: 0;
  padding-top: 80px;
  position: relative;
  @media screen and (max-width: 620px)  {
    height: 550px;
  }
  &__hexogon {
    .hexogonicon(@itemactive, 74px, 86px);
    text-align: center;
    position: absolute;
    left: 50%;
    top: 15%;
    transform: translate(-50%, -15%);
    &-border {
      z-index: 40;
      position: absolute;
      top: -20px;
      left: 0;
      .hexogonborder(lighten(@itemactive, 12%), 4px, 74px, 86px);
    }
  }
  &__slider {
    width: 600px;
    position: absolute;
    left: 49%;
    top: 90%;
    transform: translate(-49%, -90%);
    @media screen and (max-width: @largetablet)  {
      left: 50%;
      top: 90%;
      transform: translate(-50%, -90%);
    }/*
    @media screen and (max-width: 811px)  {
      margin: 40px 5% 20px 5%;
    }
    @media screen and (max-width: 745px)  {
      margin: 40px 1% 20px 1%;
    }
    position: relative;*/
    padding-top: 30px;
    &-photo {
      width: 147px;
      height: 170px;
      position: relative;
      margin-left: 5.5%;
      margin-right: 5.5%;
      div {
        width: 0;
        height: 0;
        border-width: 147px / 6 170px / 4;
        border-style: solid;
        display: block;
        position: absolute;
        z-index: 30;
      }
    }
    &-list {
      padding: 0;
    }
    &-first {
      top: 0;
      left: 0;
      border-color: white transparent transparent white;
    }
    &-second {
      top:0;
      right: 0;
      border-color: white white transparent transparent;
    }
    &-third {
      bottom: 0;
      left: 0;
      border-color: transparent transparent white white;
    }
    &-last {
      bottom: 0;
      right: 0;
      border-color: transparent white white transparent;
    }
    &-avatar {
      position: absolute;
      top: 0;
      left: 0;
      width: 147px;
      height: 170px;
      z-index: 5;
    }
    &-item {
      list-style: none;
      display: flex;
      align-items: center;
      @media screen and (max-width: 620px)  {
        flex-direction: column-reverse;
      }
    }
    &-text {
      width: 32%;
      font-size: 18px;
      letter-spacing: 0px;
      color: @bodycolor;
      font-weight: 500;
      font-family: @bodyfont;
    }
    &-title {
      font-size: 28px;
      letter-spacing: 0px;
      color: @bodycolor;
      font-weight: 500;
      margin-bottom: 10px;
      margin-top: 10px;
      font-family: @bodyfont;
    }
    &-firstname {
      color: @itemactive;
    }
    &-prof {
      margin-top: 10px;
    }
    &-nav {
      text-align: center;
      margin-top: 50px;
    }
    &-prev {
      .navbutton();
      transform: rotateZ(180deg);
      position: absolute;
      left: 43%;
      top: 100%;
      transform: translate(-43%, -100%);
    }
    &-next {
      .navbutton();
      position: absolute;
      left: 55%;
      top: 100%;
      transform: translate(-55%, -100%);
    }
  }
}
</style>
