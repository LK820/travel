<template>
    <div>
        <cityheader></cityheader>
        <cityhsearch></cityhsearch>
    </div>
</template>

<script>
    import CityHeader from './components/cityHeader'
    import CitySearch from './components/search'
    export default {
        name: "city",
        components:{
            cityheader:CityHeader,
            cityhsearch:CitySearch
        }
    }
</script>

<style scoped>

</style>