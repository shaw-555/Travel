<template>
  <div class="icons">
    <swiper>
      <swiper-slide v-for="(page, index) of pages" :key="index">
        <div
          class="icon"
          v-for="item of page"
          :key="item.id"
          >
          <div class="icon-img">
            <img class="icon-img-content" :src="item.imgUrl">
          </div>
           <p class="icon-desc">{{item.desc}}</p>
      </div>
      </swiper-slide>
      <swiper-slide>
        <div class="icon">
          <div class="icon-img">
            <img class="icon-img-content" src="">
          </div>
           <p class="icon-desc">热门景点</p>
      </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      iconList: [{
        id: '0001',
        imageUrl: `http://img1.qunarzz.com/sight/p0/
        1902/f2/f2e0213052717f7ca3.water.jpg_250x250_540fc25d.jpg`,
        desc: '景点门票'
      },
      {
        id: '0002',
        imageUrl: `http://img1.qunarzz.com/sight/p0/
        1902/f2/f2e0213052717f7ca3.water.jpg_250x250_540fc25d.jpg`,
        desc: '滑雪季节'
      },
      {
        id: '0003',
        imageUrl: `http://img1.qunarzz.com/sight/p0/
        1902/f2/f2e0213052717f7ca3.water.jpg_250x250_540fc25d.jpg`,
        desc: '泡温泉'
      },
      {
        id: '0004',
        imageUrl: `http://img1.qunarzz.com/sight/p0/
        1902/f2/f2e0213052717f7ca3.water.jpg_250x250_540fc25d.jpg`,
        desc: 'zzz'
      },
      {
        id: '0005',
        imageUrl: `http://img1.qunarzz.com/sight/p0/
        1902/f2/f2e0213052717f7ca3.water.jpg_250x250_540fc25d.jpg`,
        desc: 'aaa'
      },
      {
        id: '0006',
        imageUrl: `http://img1.qunarzz.com/sight/p0/
        1902/f2/f2e0213052717f7ca3.water.jpg_250x250_540fc25d.jpg`,
        desc: 'bbb'
      },
      {
        id: '0007',
        imageUrl: `http://img1.qunarzz.com/sight/p0/
        1902/f2/f2e0213052717f7ca3.water.jpg_250x250_540fc25d.jpg`,
        desc: 'ffff'
      },
      {
        id: '0008',
        imageUrl: `http://img1.qunarzz.com/sight/p0/
        1902/f2/f2e0213052717f7ca3.water.jpg_250x250_540fc25d.jpg`,
        desc: 'eeee'
      },
      {
        id: '0009',
        imageUrl: `http://img1.qunarzz.com/sight/p0/
        1902/f2/f2e0213052717f7ca3.water.jpg_250x250_540fc25d.jpg`,
        desc: 'zzzz'
      }]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .icons >>> .swiper-container
    height: 0
    padding-bottom: 50%
  .icons
    margin-top: .1rem
    .icon
      position: relative
      overflow: hidden
      float: left
      width: 25%
      height: 0
      padding-bottom: 25%
      .icon-img
        position: absolute
        top: 0
        left: 0
        right: 0
        bottom: .44rem
        box-sizing: border-box
        padding: .1rem
        .icon-img-content
          display: block
          margin: 0 auto
          height: 100%
      .icon-desc
        position: absolute
        left: 0
        right: 0
        bottom: 0
        height: .44rem
        line-height: .44rem
        text-align: center
        color: $darkTextColor
        ellipsis()
</style>
