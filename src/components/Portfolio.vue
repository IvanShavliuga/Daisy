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
  margin: 0;
  padding: 40px 0 40px 0;
  .headersection();
  &__title {
    width: 165px;
  }
  &__menu {
    border-top: 1px solid @bodycolor;
    border-bottom: 1px solid @bodycolor;
    padding: 5px 0;
    width: 95%;
    margin: 50px auto;
    @media screen and (max-width: 695px) {
      width: 80%;
    }
    &-list {
      display: flex;
      justify-content: center;
      padding: 0 15px;
      @media screen and (max-width: 850px) {
        justify-content: center;
        flex-wrap: wrap;
        padding: 0;
      }
      @media screen and (max-width: 695px) {
        flex-direction: column;
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
      padding: 0 10px;
      margin: 0;
      @media screen and (max-width: @largetablet) {
        padding-left: 10px;
        padding-right: 10px;
      }
      @media screen and (max-width: 800px) {
        padding-left: -20px;
        padding-right: 10px;
      }
      @media screen and (max-width: @phone) {
        width: auto;
      }
      &:after {
        content: '/';
        color: @bodycolor;
        padding-left: 20px;
        @media screen and (max-width: 695px) {
          display: none;
        }
        /*@media screen and (max-width: @largetablet) {
          padding-left: 30px;
          padding-right: 10px;
        }
        @media screen and (max-width: 850px) {
          padding-left: 10px;
          padding-right: -20px;
        }
        @media screen and (max-width: 772px) {
          display: none;
        }*/
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
    width: 95%;
    margin: 50px auto;
    @media screen and (max-width: 749px)  {
      width: 80%;
    }
    @media screen and (max-width: @phone) {
      width: auto;
    }
    &-item {
      list-style: none;
      position: relative;
      margin: 8px;
      &:first-child, &:last-child {
        .portfolio__block-img, .portfolio__block-hover {
          width: 505px;
          height: 212px;
          @media screen and (max-width: 1325px) {
            width: 355px;
          }
          @media screen and (max-width: 1021px) {
            width: 210px;
          }
          @media screen and (max-width: 949px) {
            width: 210px;
          }
          @media screen and (max-width: 954px) {
            width: 210px;
          }
          /*@media screen and (max-width: 1147px) {
            width: 245px;
          }
          @media screen and (max-width: 1109px) {
            width: 210px;
          }*/
          @media screen and (max-width: 877px) {
            width: 210px;
          }
          @media screen and (max-width: 793px) {
            width: 180px;
            height: 180px;
          }
          @media screen and (max-width: 612px) {
            width: 250px;
            height: 250px;
          }
          @media screen and (max-width: @phone) {
            width: 100%;
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
        @media screen and (max-width: 1021px) {
          width: 210px;
        }
        @media screen and (max-width: 1109px) {
          width: 210px;
        }
        @media screen and (max-width: 877px) {
          width: 210px;
        }
        @media screen and (max-width: 793px) {
          width: 180px;
          height: 180px;
        }
        @media screen and (max-width: 612px) {
          width: 250px;
          height: 250px;
        }
        @media screen and (max-width: @phone) {
          width: 100%;
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
    @media screen and (max-width: 508px) {
      margin: 30px  10% 15px 10%;
    }
    @media screen and (max-width: 270px) {
      margin: 30px  10% 15px 10%;
      width: 167px;
      height: 44px;
      font-size: 16px;
    }
  }
}
</style>
