<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe682;</div>
    </div>
    <div class="header-input">
      <div class="iconfont search-icon">&#xe613;</div>
      输入城市/游玩/景点名称
    </div>
    <router-link to="/city">
      <div class="header-right">
        {{ this.city }}
        <span class="iconfont arrow-down-icon">&#xeb6d;</span>
      </div>
    </router-link>
  </div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  name: 'home',
  computed: {
    ...mapState(['city'])
  }
}
</script>

<style lang="stylus" scoped>
@import '~$styles/varibles.styl'

.header
  display flex
  height $headerHeight
  line-height $headerHeight
  background-color $bgColor
  color #fff
  .header-left
    width $headerLeftWidth
    float left
    .back-icon
      text-align center
      font-size 0.4rem
  .header-input
    flex 1
    height 0.64rem
    line-height 0.64rem
    margin-top 0.1rem
    margin-left 0.2rem
    padding-left 0.1rem
    background-color #fff
    border-radius $borderRadius
    color #ccc
    .search-icon
      float left
      padding 0 0.1rem
      font-size 0.4rem
  .header-right
    min-width 1.04rem
    padding 0 0.1rem
    float right
    text-align center
    color #fff
    .arrow-down-icon
      font-size 0.24rem
      margin-left -0.04rem
</style>
