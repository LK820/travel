<template>
    <div class="cityList" ref="wrapper">
        <div>
            <div class="area">
                <div class="title">当前城市</div>
                <div class="button-list">
                    <div class="button-wrapper">
                        <div class="button">北京</div>
                    </div>
                </div>
            </div>
            <div class="area">
                <div class="title">热门城市</div>
                <div class="button-list">
                   <div class="button-wrapper" v-for="i of hot">
                       <div class="button">{{i.name}}</div>
                   </div>
                </div>
            </div>

            <div class="area" v-for="(i,k) of cities">
                <div class="title">{{k}}</div>
                <div class="item-list">
                    <div class="item" v-for="innerI of i">
                        {{innerI.name}}
                    </div>

                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import Bscroll from 'better-scroll'
    export default {
        name: "cityList",
        mounted(){
            this.scroll = new Bscroll(this.$refs.wrapper)
        },
        props:{
            hot:Array,
            cities:Object
        },
        data(){
            return{

            }
        }
    }
</script>

<style scoped>
    .title{
        line-height: 1.2rem;
        background: #eee;
        padding: 0.3rem 0 0.3rem 0.7rem;
        color: #666;
        border-top: 1px solid #ccc;
        border-bottom: 1px solid #ccc;
    }
    .button-list{
        padding: 0.3rem 1.3rem 0.3rem 0.3rem;
        overflow: hidden;
    }
    .button-wrapper{
        width: 33.33%;
        float: left;
    }
    .button{
        text-align: center;
        margin: 0.3rem;
        border: 1px solid #ccc;
        border-radius: 0.3rem;
        padding: 0.2rem;
    }
    .item-list .item{
        line-height: 1.8rem;
        color: #666;
        padding-left: 0.7rem;
        border-bottom:1px solid #ccc
    }
    .cityList{
        overflow: hidden;
        position: absolute;
        top: 4.7rem;
        left: 0;
        right: 0;
        bottom: 0;
    }
</style>