<template>
  <div>
    <home-header></home-header>
    <Swiper></Swiper>
    <Icons></Icons>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import Swiper from './components/Swiper'
import Icons from './components/Icons'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    Swiper,
    Icons
  }
}
</script>

<style>

</style>
