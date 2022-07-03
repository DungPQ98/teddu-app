<template>
  <div class="body-container overflow-hidden">
      <div class="flex w-full justify-center main-banner">
    <div class="flex flex-col w-full relative banner-container">
      <div class="background">
        <img
          src="~/static/images/bg.png"
          class="w-full absolute top-0 left-0 desktop"
        />
      </div>

      <div class="flex w-full justify-center relative">
        <Header />
      </div>
      <div class="flex w-full justify-start relative">
        <SideBar />
        <div class="w-full main-content">
          <nuxt />
        </div>
      </div>
    </div>
  </div>
  </div>
</template>

<script>
import Vue from 'vue'
import Header from '../components/Home/Banner/Header.vue'
import SideBar from '../components/Home/Banner/SideBar.vue'
export default Vue.extend({
  name: 'IndexPage',
  components: {
    Header,
    SideBar
},
})
</script>

<style lang="scss" scoped>
.body-container {  background: #302B27;
}
</style>

<style lang="scss">
/* .bgvid {
  inset: 0px;
  position: fixed;
  height: 100vh;
  width: 100vw;
  max-width: 100%;
  object-fit: cover;
  z-index: -1;
  user-select: none;
} */
@font-face {
  font-family: 'Langar';
  src: url(../static/fonts/Langar-Regular.ttf);
}
@font-face {
  font-family: "Monument Extended";
  src: local("Monument Extended"),
   url(../static/fonts/MonumentExtended-Regular.otf) format("truetype");
}
.font-mehu {
  font-family: "Monument Extended";
}
.desktop {
  @media only screen and (max-width: 767px) {
    display: none;
  }
}
.mobile {
  @media only screen and (min-width: 767px) {
    display: none;
  }
}
body {
  font-family: 'Langar';
  color: #FFFFFF;
}
.btn {
  min-width: 172.73px;
  height: 44.23px;
  background: #985C23;
  color: white;
  font-weight: 400;
  font-size: 20px;
  border: 4px solid #000000;
  border-radius: 8px;
  @media only screen and (max-width: 767px) {
    min-width: 81px;
    height: 28px;
    font-size: 14px;
  }
}
.banner-container {
  height: 100vh;
  .background {
    img {
      height: 100%;
    }
  }
}
</style>

<style lang="sass">
.agile
  width: 100%

  &__actions
    margin-top: 20px

  &__nav-button
    background: transparent
    border: none
    color: #ccc
    cursor: pointer
    font-size: 24px
    transition-duration: .3s

    &:hover
      color: #888

  &__dot
    margin: 0 10px

    button
      background-color: #eee
      border: none
      border-radius: 50%
      cursor: pointer
      display: block
      height: 10px
      font-size: 0
      line-height: 0
      margin: 0
      padding: 0
      transition-duration: .3s
      width: 10px

    &--current,
    &:hover
      button
        background-color: #888

// Slides styles	
.slide
  align-items: center
  color: #fff
  display: flex
  height: 300px
  justify-content: center

  h3
    font-size: 32px
    font-weight: 300

// Slides backgrounds
$colors: #f1c40f #e67e22 #e74c3c #9b59b6 #3498db #2ecc71

@for $i from 1 through length($colors)
  $color: nth($colors, $i)

  .slide--#{$i}
    background-color: $color
</style>