<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" alt="">
      </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
import { swiper, swiperSlide } from 'vue-awesome-swiper'
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        autoplay: 3000
      },
      swiperList: [
        {
          id: 1,
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1809/fc/b3f8c12b7fc6a902.jpg_750x200_194c7b39.jpg'
        },
        {
          id: 2,
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1806/ee/b889bce65d6dcf02.jpg_750x200_b1cb6a9f.jpg'
        },
        {
          id: 3,
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1809/c6/2467595fffc3b302.jpg_750x200_cca13d51.jpg'
        }
      ]
    }
  },
  components: {
    swiper,
    swiperSlide
  },
  computed: {
    swiper () {
      return this.$refs.mySwiper.swiper
    }
  },
  mounted () {
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff !important
  .wrapper
    width: 100%
    overflow: hidden
    height: 0
    padding-bottom: 26.67%
    background: #eee
    .swiper-img
      width: 100%
</style>
