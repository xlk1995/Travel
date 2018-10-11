<template>
  <div class="header">
    城市选择
    <router-link to="/">
      <div class="iconfont header-back">&#xe624;</div>
    </router-link>
  </div>
</template>

<script>
export default {
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .header
    position: relative
    height: $headerHeight
    line-height: $headerHeight
    overflow: hidden
    background: $bgcolor
    color: #ffffff
    text-align: center
    font-size: .32rem
    .header-back
      position: absolute
      top: 0
      left: 0
      font-size: .4rem
      text-align: center
      color: white
</style>
