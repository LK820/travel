<template>
    <div class="cityHeader">
        <router-link to="/">
            <span class="iconfont cityHeaderBack">&#xe624;</span>
        </router-link>
        <span>城市选择</span>
    </div>
</template>

<script>
    export default {
        name: "cityHeader"
    }
</script>

<style lang="stylus" scoped>
    .cityHeader
        overflow: hidden;
        height: 2.2rem
        line-height: 2.2rem
        text-align: center
        color: #fff
        background:#00bcd4
        font-size :1.1rem
        position: relative
        .cityHeaderBack
            width: 2rem
            text-align: center
            font-size: 1rem
            position: absolute
            left:0
            color: #fff
</style>