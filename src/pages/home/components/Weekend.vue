<template>
  <div>
    <div class="title">周末去哪儿</div>
      <ul class="border-bottom">
        <li class="item" v-for="item of recommendList" :key="item.id">
          <div class="item-img-wrapper">
            <img :src="item.imgUrl" class="item-img">
          </div>
          <div class="item-info">
            <p class="item-title">{{item.title}}</p>
            <p class="item-desc">{{item.desc}}</p>
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
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/fa/ca65fde9677de2.jpg_r_640x214_4500e3ff.jpg',
        title: '世界之窗',
        desc: '带你看世界'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/fa/ca65fde9677de2.jpg_r_640x214_4500e3ff.jpg',
        title: '世界之窗',
        desc: '带你看世界'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/fa/ca65fde9677de2.jpg_r_640x214_4500e3ff.jpg',
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
  .item-img-wrapper
    height: 0
    overflow: hidden
    padding-bottom: 33.4%
  .item-img
    width: 100%
  .item-info
    padding: .1rem
    .item-title
      line-height: .54rem
      font-size : .32rem
      ellipsis()
    .item-desc
      line-height : .4rem
      color: #cccccc
      ellipsis()
</style>
