<template>
  <div class="list">
    <div class="item">A</div>
    <div class="item">A</div>
    <div class="item">A</div>
    <div class="item">A</div>
    <div class="item">A</div>
    <div class="item">A</div>
    <div class="item">A</div>
  </div>
</template>

<script>
export default {
  name: 'CityAlphabet'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .list
   display: flex
   flex-direction: column
   justify-content : center
   position: absolute
   right:0
   top: 1.58rem
   bottom: 0
   width: .4rem
   background-color #f00
    .item
      line-height: .4rem
      text-align: center
</style>
