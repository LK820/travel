<template>
    <div>
        <homeheader :city="city"></homeheader>
        <swiper :list="swiperList"></swiper>
        <icon :list="iconList"></icon>
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
    import axios from 'axios'
    export default {
        name: "home",
        components:{
            homeheader:Header,
            swiper:Swiper,
            icon:Icon,
            recomment:Recommend,
            weekend:Weekend
        },
        data () {
            return {
                baseUrl: process.env.BASE_URL,
                city:'',
                swiperList:[{
                    id:'01',
                    img_url:require("../../assets/img/01.jpg")
                },{
                    id:'02',
                    img_url:require("../../assets/img/02.jpg")
                },{
                    id:'03',
                    img_url:require("../../assets/img/01.jpg")
                },{
                    id:'04',
                    img_url:require("../../assets/img/02.jpg")
                }],
                iconList:[{
                    id:'01',
                    img_url:require("../../assets/img/jar.png"),
                    description:"出境游"
                },{
                    id:'01',
                    img_url:require("../../assets/img/cup.png"),
                    description:"热门风景"
                },{
                    id:'01',
                    img_url:require("../../assets/img/knife.png"),
                    description:"美食林"
                },{
                    id:'01',
                    img_url:require("../../assets/img/mw.png"),
                    description:"超级巴士"
                },{
                    id:'01',
                    img_url:require("../../assets/img/eggbeater.png"),
                    description:"攻略"
                },{
                    id:'01',
                    img_url:require("../../assets/img/trash.png"),
                    description:"汽车票"
                },{
                    id:'01',
                    img_url:require("../../assets/img/rolling.png"),
                    description:"国内游"
                },{
                    id:'01',
                    img_url:require("../../assets/img/urn.png"),
                    description:"签证"
                }]
            }
        },
        methods:{
            getHomeInfo(){
                axios.get(this.baseUrl+"mock/index.json").then(this.getHomeInfoSuccess)
            },
            getHomeInfoSuccess(res){
                var data = res.data
                this.city = data.data.city
            }
        },
        mounted(){
            this.getHomeInfo()
        }
    }
</script>

<style scoped>

</style>