<template>
    <div class="citySearch">
        <input class="searchInput" type="text" placeholder="输入城市名">
    </div>
</template>

<script>
    export default {
        name: "citySearch"
    }
</script>

<style lang="stylus" scoped>
    .citySearch
        height: 1.7rem
        padding: 0.3rem
        background: #00bcd4
        .searchInput
            height: 1.8rem
            line-height: 1.8rem
            width: 100%
            text-align: center
            border:none
            border-radius :0.3rem
            padding: 0.3rem
            box-sizing :border-box
</style>