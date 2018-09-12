<template>
    <div>
        <homeheader></homeheader>
        <swiper></swiper>
        <icon></icon>
        <recomment></recomment>
        <weekend></weekend>
    </div>
</template>

<script>
    import Header from './components/header'
    import Swiper from './components/swiper'
    import Icon from './components/icon'
    import Recommend from './components/recommend'
    import Weekend from './components/weekend'
    export default {
        name: "home",
        components:{
            homeheader:Header,
            swiper:Swiper,
            icon:Icon,
            recomment:Recommend,
            weekend:Weekend
        }
    }
</script>

<style scoped>

</style>