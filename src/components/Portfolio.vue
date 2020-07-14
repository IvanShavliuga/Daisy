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
      <!--<li class="portfolio__block-item">
        <div class="portfolio__block-hover"
          v-show="(showid==true)&&(id==0)"
          v-on:mouseleave="showid=false; id=-1"
          >
          <h4 class="portfolio__block-title">
            portfolio #1
          </h4>
        </div>
        <img
          class="portfolio__block-img"
          src="../assets/images/portfolio_1.png"
          alt="Portfolio #1"
          v-on:mouseover="showid=true; id=0"
        >
      </li>
      <li class="portfolio__block-item">
        <div class="portfolio__block-hover"
          v-show="(showid==true)&&(id==1)"
          v-on:mouseleave="showid=false; id=-1">
          <h4 class="portfolio__block-title">
            portfolio #2
          </h4>
        </div>
        <img
          class="portfolio__block-img"
          src="../assets/images/portfolio_2.png"
          alt="Portfolio #2"
          v-on:mouseover="showid=true; id=1">
      </li>
      <li class="portfolio__block-item">
        <div class="portfolio__block-hover">
          <h4 class="portfolio__block-title">
            portfolio #3
          </h4>
        </div>
        <img
          class="portfolio__block-img"
          src="../assets/images/portfolio_3.png"
          alt="Portfolio #3">
      </li>
      <li class="portfolio__block-item">
        <div class="portfolio__block-hover">
          <h4 class="portfolio__block-title">
            portfolio #4
          </h4>
        </div>
        <img
          class="portfolio__block-img"
          src="../assets/images/portfolio_4.png"
          alt="Portfolio #4">
      </li>
      <li class="portfolio__block-item">
        <div class="portfolio__block-hover">
          <h4 class="portfolio__block-title">
            portfolio #5
          </h4>
        </div>
        <img
          class="portfolio__block-img"
          src="../assets/images/portfolio_5.png"
          alt="Portfolio #5">
      </li>
      <li class="portfolio__block-item">
        <div class="portfolio__block-hover">
          <h4 class="portfolio__block-title">
            portfolio #6
          </h4>
        </div>
        <img
          class="portfolio__block-img"
          src="../assets/images/portfolio_6.png"
          alt="Portfolio #6">
      </li>-->
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
import img1 from '../assets/images/portfolio_1.png'
import img2 from '../assets/images/portfolio_2.png'
import img3 from '../assets/images/portfolio_3.png'
import img4 from '../assets/images/portfolio_4.png'
import img5 from '../assets/images/portfolio_5.png'
import img6 from '../assets/images/portfolio_6.png'
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
  width: 100% -40px;
  height: 100% -160px;
  margin: 0;
  padding: 80px 20px 80px 20px;
  .headersection();
  &__title {
    width: 165px;
    margin: 0 auto;
  }
  &__menu {
    border-top: 1px solid @bodycolor;
    border-bottom: 1px solid @bodycolor;
    padding: 5px 0;
    margin-top: 50px;
    margin-bottom: 40px;
    &-list {
      display: flex;
      justify-content: space-between;
      padding: 0 25px;
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
      &:after {
        content: '/';
        color: @bodycolor;
        padding-left: 60px;
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
        }
      }
      &:first-child, &nth-child(4) {
        margin-left: 0;
      }
      &:last-child, &nth-child(3) {
        margin-right: 0;
      }
    }
    &-hover {
      position: absolute;
      left: 0;
      top: 0;
      width: 245px;
      height: 212px;
      background-color: @itemactive;
      color: white;
      opacity: 0.6;
      z-index: 20;
      font-size: 28px;
      letter-spacing: 0px;
      line-height: 26px;
      font-weight: bold;
      font-family: @bodyfont;
    }
    &-img {
      width: 245px;
      height: 212px;
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
