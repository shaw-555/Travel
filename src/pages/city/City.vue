<template>
  <div>
    <city-header/>
    <city-search/>
  </div>
</template>

<script>
import CityHeader from './components/header'
import CitySearch from './components/Search'

export default {
  name: 'City',
  components: {
    CityHeader,
    CitySearch
  }
}
</script>

<style lang="stylus" scoped>

</style>
