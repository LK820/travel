<template>
    <div>
        <cityheader></cityheader>
        <cityhsearch></cityhsearch>
        <citylist :hot="hotcities" :cities="cities"></citylist>
        <alphabet :alphabetList="cities"></alphabet>
    </div>
</template>

<script>
    import axios from 'axios'
    import CityHeader from './components/cityHeader'
    import CitySearch from './components/search'
    import CityList from './components/list'
    import Alphabet from './components/alphabet'

    export default {
        name: "city",
        components: {
            cityheader: CityHeader,
            cityhsearch: CitySearch,
            citylist: CityList,
            alphabet: Alphabet
        },
        data() {
            return {
                cities: {},
                hotcities: []
            }
        },
        methods: {
            getCity() {
                var _this = this;
                axios.get('mock/index.json').then(function(res){
                    _this.hotcities = res.data.cityList.data.hotCities;
                    _this.cities = res.data.cityList.data.cities;
                })
            }
        },
        mounted() {
            //挂载成功时执行
            this.getCity()
        }
    }
</script>

<style scoped>

</style>