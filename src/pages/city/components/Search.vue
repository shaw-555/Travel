import CityHeader from '.components/city';
<template>
  <div>
    <div class="search">
      <input v-model="keyword" class="search-input" type="text" placeholder="输入城市名或拼音">
    </div>
    <div class="search-content" v-show="keyword.length>0" ref="search">
      <ul>
        <li
        class="search-item border-bottom"
        v-for="item of list"
        :key="item.id"
        @click="handleCityClick(item.name)"
        >
          {{item.name}}</li>

        <li class="search-item border-bottom" v-show="hasNoData">没有找到匹配数据</li>
      </ul>
    </div>
  </div>
</template>

<script>
import Bscroll from 'better-scroll'
import { mapMutations } from 'vuex'

export default {
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
import { mapMutations } from 'vuex'
  .search
    height: .72rem
    background: $bgColor
    padding: 0 .1rem
    .search-input
      box-sizing: border-box
      height: .62rem
      line-height: .62rem
      padding: 0 .1rem
      width: 100%
      text-align: center
      border-radius: .06rem
      color: #666
  .search-content
    background-color: red
    position: absolute
    top: 1.58rem
    left: 0
    right: 0
    bottom: 0
    z-index: 100
    .search-item
      text-align: left
      line-height: .62rem
      padding-left: .2rem
      background-color #fff
      color: #666
      z-index: 110
</style>
