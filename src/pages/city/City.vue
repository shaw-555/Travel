<template>
  <div>
    <city-header/>
    <city-search/>
    <city-list :list="hotCities" :normalCity="normalCities"/>
    <city-alphabet/>
  </div>
</template>

<script>
import CityHeader from './components/header'
import CitySearch from './components/Search'
import CityList from './components/List'
import CityAlphabet from './components/Alphabet'
import axios from 'axios'

export default {
  name: 'City',
  components: {
    CityHeader,
    CitySearch,
    CityList,
    CityAlphabet
  },
  data () {
    return {
      hotCities: [{}],
      normalCities: {}
    }
  },
  methods: {
    getCityInfo () {
      axios.get('/api/city.json')
        .then(this.handleGetCityInfoSucc)
    },
    handleGetCityInfoSucc (res) {
      let data = res.data.data
      this.hotCities = data.hotCities
      this.normalCities = data.cities
      console.log(this.normalCities)
      console.log(Object.keys(this.normalCities))
    }
  },
  mounted () {
    this.getCityInfo()
  }
}
</script>

<style lang="stylus" scoped>

</style>
