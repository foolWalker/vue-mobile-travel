<template>
  <div class="header">
    <div class="header-left">
      <span class="iconfont icon-fanhui"></span>
    </div>
    <div class="header-input"><span class="iconfont icon-sousuo"></span>输入城市/景点/游玩主题</div>
    <router-link to="/city">
      <div class="header-right">{{city}}<span class="iconfont icon-jiantouxia"></span></div>
    </router-link>
  </div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  name: 'HomeHeader',
  computed: {
    ...mapState(['city'])
  },
  mounted () {
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varible.styl'
  .header
    display: flex
    height: .86rem
    line-height: .86rem
    background: $bgColor
    color: #fff
    text-align: center
    &-left
      width: .64rem
      float: left
      .icon-fanhui
        font-size: .36rem
    &-right
      min-width: 1.04rem
      padding: 0 .1rem
      float: right
      color: #fff
      .icon-jiantouxia
        font-size: .24rem
        margin-left: .04rem
    &-input
      flex: 1
      height: .64rem
      line-height: .64rem
      margin-left: .2rem
      margin-top: .12rem
      border-radius: .06rem
      background: #fff
      color: #e4e7ea
      text-align: left
      .icon-sousuo
        margin-left: .2rem
        margin-right: .1rem
</style>
