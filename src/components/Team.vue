<template>
  <section class="team">
    <div class="wrapper">
      <h2 class="team__title">
        Our
        <span class="team__title-lastword">team</span>
      </h2>
      <ul class="team__block">
        <li class="team__block-item"
            v-for="(u,k) in users"
            :key="k"
        >
          <div class="team__block-hexogon">
            <img  class="team__block-avatar" :src="u.avatar" :alt="u.firstname+' '+u.lastname">
            <div class="team__block-first"></div>
            <div class="team__block-second"></div>
            <div class="team__block-third"></div>
            <div class="team__block-last"></div>
          </div>
          <h4 class="team__block-name">
            <span class="team__block-firstname">
              {{u.firstname}}
            </span>
            {{u.lastname}}
          </h4>
          <p class="team__block-prof">{{u.prof}}</p>
          <p class="team__block-social">
            <i class="team__block-twitter"></i>
            <i class="team__block-facebook"></i>
            <i class="team__block-linkedin"></i>
          </p>
        </li>
      </ul>
    </div>
  </section>
</template>
<script>
import img1 from '../assets/images/team_1.png'
import img2 from '../assets/images/team_2.png'
import img3 from '../assets/images/team_3.png'
export default {
  name: 'Team',
  data () {
    return {
      users: [{
        firstname: 'Tomothy',
        lastname: 'Bowman',
        prof: 'Marketing',
        avatar: img1
      }, {
        firstname: 'Steve',
        lastname: 'Tracy',
        prof: 'CEO',
        avatar: img2
      }, {
        firstname: 'Hellen',
        lastname: 'Johns',
        prof: 'Clients',
        avatar: img3
      }]
    }
  }
}
</script>
<style lang="less">
.team {
  width: 100%;
  height: 517px;
  margin: 0;
  padding-top: 40px;
  background-color: @bodygraybg;
  .headersection();
  &__title {
    width: 150px;
  }
  &__block {
    display: flex;
    justify-content: space-around;
    padding-top: 40px;
    width: 80%;
    margin-left: 7%;
    &-item {
      position: relative;
      list-style: none;
      width: 230px;
    }
    &-hexogon {
      width: 147px;
      height: 170px;
      position: relative;
      margin-left: 18%;
      margin-right: 18%;
      @media screen and (min-width: 1400px) {
        width: 153px;
        height: 171px;
        top: -5px;
        position: relative;
        margin-left: 27%;
        padding: 0;
        left: -12px;
      }
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
    &-first {
      top: 0;
      left: 0;
      border-color: @bodygraybg transparent transparent @bodygraybg;
    }
    &-second {
      top:0;
      right: 0;
      border-color: @bodygraybg @bodygraybg transparent transparent;
    }
    &-third {
      bottom: 0;
      left: 0;
      border-color: transparent transparent @bodygraybg @bodygraybg;
    }
    &-last {
      bottom: 0;
      right: 0;
      border-color: transparent @bodygraybg @bodygraybg transparent;
    }
    &-avatar {
      position: absolute;
      top: 0;
      left: 0;
      width: 147px;
      height: 170px;
      z-index: 5;
    }
    &-firstname {
      color: @itemactive;
    }
    &-name {
      font-size: 28px;
      letter-spacing: 0px;
      line-height: 26px;
      color: @bodycolor;
      font-weight: 500;
      font-family: @bodyfont;
      text-align: center;
      margin: 10px 0;
    }
    &-prof {
      font-size: 28px / 1.5;
      letter-spacing: 0px;
      line-height: 26px;
      color: @bodycolor;
      font-weight: 500;
      font-family: @bodyfont;
      margin: 10px 0;
      text-align: center;
    }
    &-social {
      margin: 10px 0;
      height: 37px;
      text-align: center;
      i {
        height: 37px;
        width: 37px;
        background-repeat: no-repeat;
        background-position: center center;
        border-radius: 50%;
        display: inline-block;
        margin-right: 10px;
        &:last-child {
          margin-right: 0;
        }
        &:hover {
          background-color: @itemactive;
        }
      }
    }
    &-twitter {
      background-image: url('../assets/images/twitter.svg')
    }
    &-facebook {
      background-image: url('../assets/images/facebook.svg')
    }
    &-linkedin {
      background-image: url('../assets/images/linkedin.svg')
    }
  }
}
</style>
