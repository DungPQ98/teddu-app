<template>
  <div class="flex w-full h-full relative justify-between main-header">
    <div class="logo z-10">
      <img src="~/static/icons/logo.svg" />
    </div>
    <div class="main-menu flex z-10">
      <a
        v-for="(item, index) in data"
        :key="index"
        :href="item.link"
        target="_blank"
      >
        <img :src="item.icon" alt="" />
      </a>
      <button class="btn move-to-earn">Teddinu</button>
      <button class="btn move-to-earn connect-wallet">Connect wallet</button>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  name: 'NuxtHeader',
  data() {
    return {
      data: [
        {
          link: '',
          icon: require('~/static/icons/mail.png'),
        },
        {
          link: '',
          icon: require('~/static/icons/tele.png'),
        },
        {
          link: '',
          icon: require('~/static/icons/tele.png'),
        },
        {
          link: '',
          icon: require('~/static/icons/twiter.png'),
        },
      ],
    }
  },
})
</script>

<style lang="scss" scoped>
.main-header {
  background: #130a02;
  max-width: 1920px;
  .logo {
    padding-top: 37px;
    padding-left: 36px;
    @media only screen and (max-width: 767px) {
      padding-top: 16px;
      padding-left: 10px;
      max-width: 65px;
    }
  }
  .flag {
    height: 40px;
    @media only screen and (max-width: 767px) {
      height: 28px;
    }
  }
  .main-menu {
    padding-top: 18px;
    padding-right: 25px;
    font-size: 14px;
    padding-bottom: 20px;
    align-items: center;
    a {
      max-width: 64px;
      margin-right: 30px;
    }
    @media only screen and (max-width: 767px) {
      padding-top: 16px;
      padding-right: 16px;
      font-size: 12px;
    }
    .menu {
      min-width: 93px;
      height: 40px;
      color: #142e38;
      border: 1px solid #142e38;
      border-radius: 4px;
      margin-left: 12px;
      font-weight: 600;
      @media only screen and (max-width: 767px) {
        min-width: 65px;
        height: 28px;
      }
      img {
        padding-right: 9px;
        @media only screen and (max-width: 767px) {
          padding-right: 4px;
        }
      }
    }
    .move-to-earn {
      width: 231.59px;
      height: 70.77px;
      background: #985c23;
      color: white;
      margin-left: 18px;
      font-weight: 400;
      font-size: 30px;
      border: 2px solid rgba(255, 255, 255, 0.25);
      border-radius: 12px;
    }
    .connect-wallet {
      background: #5794cc;
    }
  }
}
.menu-center {
  align-items: self-end;
}
.menu-btn {
  padding: 0 30px;
  font-size: 24px;
  font-weight: 400;
  color: #ffffff;
  .img-docs {
    padding-left: 7px;
  }
}
</style>