<template>
  <ul class="list">
    <li class="item" v-for="(item, key) of cities" :key="key">{{key}}</li>
  </ul>
</template>

<script>
export default {
  name: 'CityAlphabet',
  props: {
    cities: Object
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .list
   display: flex
   flex-direction: column
   justify-content : center
   position: fixed
   right:0
   top: 1.58rem
   bottom: 0
   width: .4rem
   background-color #f00
    .item
      line-height: .4rem
      text-align: center
</style>
