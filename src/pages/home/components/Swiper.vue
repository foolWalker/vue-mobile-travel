<template>
  <div class="wrapper" v-if="showSwiper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" alt="">
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  props: {
    swiperList: Array
  },
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        autoplay: 3000
      }
    }
  },
  computed: {
    showSwiper () {
      return this.swiperList.length
    }
  },
  mounted () {
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination
    bottom: 5px
    .swiper-pagination-bullet-active
      background: #fff !important
  .wrapper
    width: 100%
    overflow: hidden
    height: 0
    padding-bottom: 31.25%
    background: #eee
    .swiper-img
      width: 100%
</style>
