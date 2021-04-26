<template>
  <div class="icons">
    <div class="icon">
      <div class="icon-img">
        <img class="icon-img-content" src="">
      </div>
      <p class="icon-desc">热门景点</p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl';
  .icons
    width: 100%
    height: 0
    padding-bottom: 50%
    overflow: hidden
    background-color: #eee
    .icon
      position: relative
      overflow: hidden
      float: left
      width: 25%
      height: 0
      padding-bottom: 25%
      background-color: #f00
      .icon-img
        position: absolute
        top: 0
        left: 0
        right: 0
        background-color #fff
        bottom: .44rem
        padding: .1rem
        .icon-img-content
          display: block
          margin: 0 auto
          height: 100%
      .icon-desc
        position: absolute
        left: 0
        bottom:0
        right: 0
        color: $darkTextColor
        text-align: center
</style>
