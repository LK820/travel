<template>
    <div>
        <homeheader></homeheader>
        <swiper></swiper>
        <icon></icon>
    </div>
</template>

<script>
    import Header from './components/header'
    import Swiper from './components/swiper'
    import Icon from './components/icon'
    export default {
        name: "home",
        components:{
            homeheader:Header,
            swiper:Swiper,
            icon:Icon
        }
    }
</script>

<style scoped>

</style>