<template>
    <div class="header">
        <div class="header-left">
            <span class="iconfont back_icon">&#xe624;</span>
        </div>
        <div class="header-input"><span class="iconfont">&#xe632;</span>输入城市/景点/游玩主题</div>
        <router-link to="/city">
            <div class="header-right">
                <span>{{this.city}}</span>
                <span class="iconfont arrow_icon">&#xe600;</span>
            </div>
        </router-link>
    </div>
</template>

<script>
    export default {
        name: "homeheader",
        props:{
            city:String
        }
    }
</script>

<style lang="stylus" scoped>
    @import "~@/assets/styles/var.styl"
    .header
        display:flex
        height: 2.5rem
        background: $bgColor
        color:#fff
        align-items :center
        .header-left
            width:2.74rem
            float:left
            .back_icon
                font-weight:bold
                padding-left :0.8rem
        .header-input
            flex:1
            border-radius :0.2rem
            height: 1.8rem
            line-height: 1.8rem
            /*align-self :center*/
            background: #fff
            color:#ccc
            padding-left: 0.5rem
            font-size :0.8rem
        .header-right
            float: right
            width: 4rem
            color:#fff
            text-align: center
            .arrow_icon
                font-size :0.6rem
</style>