<template>
    <div>
        <div class="header">
          <div class="header-left">
            <div class="iconfont back-icon" @click="test">&#xe624;</div>
          </div>
          <div class="header-input">
            <span class="iconfont">&#xe632;</span>
            输入城市/景点/游玩主题</div>
          <router-link to="/city">
            <div class="header-right">
              {{this.$store.state.city}}
              <span class="iconfont arrow-icon">&#xe64a;</span>
            </div>
          </router-link>
        </div>
    </div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  name: 'HomeHeader',
  computed: {
    ...mapState(['city'])
  },
  methods: {
    test () {
      this.$router.push('/detail')
      console.log(1)
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .header
    display: flex
    height: $headerHeight
    line-height: $headerHeight
    background: $bgColor
    color: #fff
    .header-left
      width: .64rem
      float: left
      .back-icon
        text-align: center
        font-size: .4rem
    .header-input
      flex: 1
      background: #fff
      border-radius: .1rem
      margin-top: .12rem
      height: .64rem
      margin-left: .2rem
      padding-left: .2rem
      color: #ccc
      line-height: .64rem
    .header-right
      color: #fff
      min-with: 1.04rem
      float: right
      padding: 0 .1rem
      text-align: center
      padding-left: .1rem
      .arrow-icon
       font-size: .24rem
</style>
