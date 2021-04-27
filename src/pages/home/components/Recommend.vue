<template>
  <div>
    <div class="recommend-title">热销推荐</div>
    <ul v-for="item in recommendList" :key="item.id">
      <li class="item border-bottom">
          <img :src="item.imgUrl" class="item-img">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="itme-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  props: {
    recommendList: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .recommend-title
    margin-top: .2rem
    line-height: .8rem
    background-color #eee
    text-indent: .2rem
  .item
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
        font-size: .32rem
        ellipsis()
      .item-desc
        line-height: .4rem
        color: #eee
        ellipsis()
      .item-button
        line-height: .44rem
        background-color: orange
        margin-top: .16rem
        padding: 0.1rem
        border-radius: .06rem
        color: #fff
</style>
