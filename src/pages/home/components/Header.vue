<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入城市/景点/游玩主题
    </div>
    <router-link to="/city">
      <div class="header-right">
        {{this.city}}
        <span class="iconfont arrow-icon">&#xe64a;</span>
      </div>
    </router-link>
  </div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  name: 'HomeHeader',
  computed: {
    ...mapState(['city'])
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .icon
    width: 1em
    height: 1em
    vertical-align: -0.15em
    fill: currentColor
    overflow: hidden
  .header
    display: flex
    line-height: $headerHeight
    height: $headerHeight
    background: $bgcolor
    color: #fff
    .header-left
      width: .64rem
      .back-icon
        text-align: center
        font-size : .4rem
    .header-input
      flex: 1
      height : .64rem
      line-height : .64rem
      margin-top : .12rem
      margin-left: .2rem
      padding-left: .2rem
      background : #ffffff
      border-radius: .1rem
      color: #cccccc
    .header-right
      min-width: 1.04rem
      padding: 0 .1rem
      text-align: center
      color: white
      .arrow-icon
        margin-left : -.04rem
        font-size : .2rem
</style>
