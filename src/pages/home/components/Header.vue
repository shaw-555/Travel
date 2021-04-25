<template>
    <div>
        <div class="header">
          <div class="header-left">left</div>
          <div class="header-input">输入城市/景点/游玩主题</div>
          <div class="header-right">right</div>
        </div>
    </div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
  .header
    display: flex
    height: .86rem
    line-height: .86rem
    background: #00bcd4
    color: #fff
    .header-left
      width: .64rem
      float: left
    .header-input
      flex: 1
      background: #fff
      border-radius: .1rem
      margin-top: .12rem
      height: .64rem
      margin-left: .2rem
      color: #ccc
      line-height: .64rem
    .header-right
      with: 1.24rem
      float: right
      text-align: center
</style>
