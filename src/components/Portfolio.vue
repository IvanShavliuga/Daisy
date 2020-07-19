<template>
<section class="portfolio">
  <div class="wrapper">
    <h2 class="portfolio__title">
      portfolio
    </h2>
    <nav class="portfolio__menu">
      <ul class="portfolio__menu-list">
        <li class="portfolio__menu-item">all</li>
        <li class="portfolio__menu-item">entertainment</li>
        <li class="portfolio__menu-item">sport</li>
        <li class="portfolio__menu-item">business</li>
        <li class="portfolio__menu-item">building</li>
      </ul>
    </nav>
    <ul class="portfolio__block">
    <li class="portfolio__block-item"
        v-for="(p,k) in pictures"
        :key="k"
    >
      <div class="portfolio__block-hover"
        v-show="(showid==true)&&(id==k)"
        v-on:mouseleave="showid=false; id=-1"
        >
        <h4 class="portfolio__block-title">
          portfolio #{{k+1}}
        </h4>
        <button class="portfolio__block-button">+</button>
      </div>
      <img class="portfolio__block-img"
        :src="p"
        :alt="'Portfolio #'+(k+1)"
        v-on:mouseover="showid=true; id=k">
      </li>
    </ul>
    <button class="portfolio__button">I want landing page</button>
  </div>
</section>
</template>
<script>
import img1 from '../assets/images/portfolio_1.jpg'
import img2 from '../assets/images/portfolio_2.jpg'
import img3 from '../assets/images/portfolio_3.jpg'
import img4 from '../assets/images/portfolio_4.jpg'
import img5 from '../assets/images/portfolio_5.jpg'
import img6 from '../assets/images/portfolio_6.jpg'
export default {
  name: 'Portfolio',
  data () {
    return {
      showid: false,
      id: -1,
      pictures: [img1, img2, img3, img4, img5, img6]
    }
  }
}
</script>
<style lang="less">
.portfolio {
  width: 850px;
  height: 845px;
  margin: 0 auto;
  padding: 40px 20px 40px 20px;
  @media screen and (max-width: 824px) {
    height: 1040px;
  }
  .headersection();
  &__title {
    width: 165px;
  }
  &__menu {
    border-top: 1px solid @bodycolor;
    border-bottom: 1px solid @bodycolor;
    padding: 5px 0;
    margin-top: 50px;
    margin-bottom: 40px;
    width: 845px;
    &-list {
      display: flex;
      justify-content: space-between;
      padding: 0 25px;
      @media screen and (max-width: @tablet) {
        justify-content: center;
        flex-wrap: wrap;
        padding: 0 5px;
      }
    }
    &-item {
      list-style: none;
      font-size: 20px;
      letter-spacing: 0px;
      line-height: 26px;
      color: @itemactive;
      font-weight: 300;
      font-family: @bodyfont;
      text-align: center;
      text-transform: uppercase;
      @media screen and (max-width: @largetablet) {
        padding-left: 10px;
        padding-right: 10px;
      }
      &:after {
        content: '/';
        color: @bodycolor;
        padding-left: 60px;
        @media screen and (max-width: @largetablet) {
          padding-left: 10px;
          padding-right: 10px;
        }
        font-size: 20px;
        font-size: bold;
      }
      &:last-child {
        &:after {
          display: none;
        }
      }
    }
  }
  &__block {
    position: relative;
    display: flex;
    flex-wrap: wrap;
    padding: 0;
    &-item {
      list-style: none;
      position: relative;
      margin: 8px;
      &:first-child, &:last-child {
        .portfolio__block-img, .portfolio__block-hover {
          width: 505px;
          height: 212px;
          @media screen and (max-width: @desktop) {
            width: 405px;
            height: 212px;
          }
          @media screen and (min-width: 1088px) {
            width: 355px;
            height: 212px;
          }
          @media screen and (max-width: 1087px) {
            width: 245px;
            height: 212px;
          }
          @media screen and (max-width: 822px) {
            width: 210px;
          }
          @media screen and (max-width: 720px) {
            width: 260px;
          }
          @media screen and (max-width: 720px) {
            width: 260px;
          }
        }
      }
      &:first-child, &nth-child(4) {
        margin-left: 0;
      }
      &:last-child, &nth-child(3) {
        margin-right: 0;
      }
      .portfolio__block-img, .portfolio__block-hover {
        width: 245px;
        height: 212px;
        @media screen and (max-width: 822px) {
          width: 210px;
        }
        @media screen and (max-width: 720px) {
          width: 260px;
        }
      }
    }
    &-hover {
      position: absolute;
      left: 0;
      top: 0;
      background-color: rgba(@itemactive, 0.6);
      color: white;
      z-index: 20;
      font-size: 28px;
      letter-spacing: 0px;
      line-height: 26px;
      font-weight: bold;
      font-family: @bodyfont;
    }
    &-title {
      margin: 20px;
      font-size: 28px;
      letter-spacing: 0px;
      line-height: 26px;
      color: #ffffff;
      font-weight: bold;
      font-family: @bodyfont;
    }
    &-button {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      background-color: transparent;
      color: white;
      border: none;
      font-size: 105px / 1.5;
      letter-spacing: -1px;
      line-height: 136px;
      color: #ffffff;
      font-weight: bold;
      font-family: @bodyfont;
    }
  }
  &__button {
    position: relative;
    width: 187px;
    height: 44px;
    border-radius: 7px;
    background-color: @itemactive;
    color: #fff;
    border: none;
    font-size: 20px;
    letter-spacing: 0px;
    line-height: 26px;
    color: @bodygraybg;
    font-weight: 300;
    font-family: @bodyfont;
    margin: 30px  40% 15px 40%;
  }
}
</style>
