<template>
    <div>
        <homeheader></homeheader>
        <swiper></swiper>
    </div>
</template>

<script>
    import Header from './components/header'
    import Swiper from './components/swiper'
    export default {
        name: "home",
        components:{
            homeheader:Header,
            swiper:Swiper
        }
    }
</script>

<style scoped>

</style>