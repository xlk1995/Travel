<template>
  <div>
    <div class="title">猜你喜欢</div>
      <ul class="border-bottom">
        <li class="item" v-for="item of recommendList" :key="item.id">
          <img :src="item.imgUrl" class="item-img">
          <div class="item-info">
            <p class="item-title">{{item.title}}</p>
            <p class="item-desc">{{item.desc}}</p>
            <button class="item-button">查看详情</button>
          </div>
        </li>
      </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1809/87/8796d4dfe0366858a3.water.png_200x200_ca6e25bf.png',
        title: '世界之窗',
        desc: '带你看世界'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1809/87/8796d4dfe0366858a3.water.png_200x200_ca6e25bf.png',
        title: '世界之窗',
        desc: '带你看世界'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1809/87/8796d4dfe0366858a3.water.png_200x200_ca6e25bf.png',
        title: '世界之窗',
        desc: '带你看世界'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    margin-top: .2rem
    line-height: .8rem
    background: #eeeeee
    text-indent: .2rem
  .item
    overflow: hidden
    display: flex
    height: 1.9rem
    .item-img
      width: 1.7rem
      height: 1.7rem
      padding: .1rem
    .item-info
      flex: 1
      padding: .1rem
      min-width: 0
      .item-title
        line-height: .54rem
        font-size : .32rem
        ellipsis()
      .item-desc
        line-height : .4rem
        color: #cccccc
        ellipsis()
      .item-button
        line-height : .44rem
        margin-top: .16rem
        background : #ff9300
        padding: 0 .2rem
        border-radius: .06rem
        color: #fff
</style>
