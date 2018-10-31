<template>
  <div class="d-flex h-100">
    <TheHeader/>
    <div class="page-wrapper">
    <transition name="fade-top">
      <nuxt/>  
    </transition>
    </div>
  </div>
</template>
<script>
import TheHeader from "~/components/TheHeader.vue"
  
  export default {
  components: {
    TheHeader
  }
}
</script>
<style lang="scss">
body {
  font-size: 14px;
  line-height: 2;
  letter-spacing: 1.1px;
  font-weight: 400;
  font-family: europa, sans-serif;
  min-height: 100vh;
  background-color: #242424;
  color: #ffffff;

  /* nav and & #F32550 */
  /*

  font-weight: 700;

  font-style: normal;*/

}

a{
  color: #fff;
  position: relative;



  &:hover {
    color: #fff;
    text-decoration: none;

    &:after {
      background-position-x: 60%;
    }
  }

  &.nuxt-link-active {
    font-weight: 700;
    color: #F32550;
  }

  &:after {
    transition-timing-function: ease;
    transition: 0.6s;
    position: absolute; 
    bottom: -10px;
    left: 0;
    width: 100%;
    height: 5px;
    content: ' ';
    background-image: url('./../static/wobble.svg');
    background-size: cover;
    background-position: 50% 50%;
  }
}

h1 {
  font-weight: 700;
  font-family: "europa",sans-serif;
  font-size: 5.5em;
  letter-spacing: 1.1px;
}

.page-wrapper {
  min-height: 100vh;
  width: 100%;
}

.fade-top-enter-active, .fade-top-leave-active {
  transition: .6s;
  transform: translateY(0px);
  opacity: 1;
}
.fade-top-enter, .fade-top-leave-to /* .fade-leave-active below version 2.1.8 */ {
  opacity: 0;
  transform: translateY(-20px);
}

</style>
