<template>
    <div class="icons">
        <swiper class="swipper" :options="swiperOption" >
            <swiper-slide >
                <div class="box">
                    <div class="img_box" v-for="i of iconList">
                        <img class="img-content" :src="i.img_url">
                        <p>{{i.description}}</p>
                    </div>
                </div>
            </swiper-slide>


            <swiper-slide >
                <div class="box">
                    <div class="img_box" v-for="i of iconList">
                        <img class="img-content" :src="i.img_url">
                        <p>{{i.description}}</p>
                    </div>

                </div>
            </swiper-slide>
            <!-- Optional controls -->
            <div class="swiper-pagination"  slot="pagination"></div>
        </swiper>

    </div>
</template>

<script>
    export default {
        name: "icon",
        data (){
            return{
                swiperOption: {
                    loop:true
                },
                iconList:[{
                    id:'01',
                    img_url:require("../../../assets/img/jar.png"),
                    description:"出境游"
                },{
                    id:'01',
                    img_url:require("../../../assets/img/cup.png"),
                    description:"热门风景"
                },{
                    id:'01',
                    img_url:require("../../../assets/img/knife.png"),
                    description:"美食林"
                },{
                    id:'01',
                    img_url:require("../../../assets/img/mw.png"),
                    description:"超级巴士"
                },{
                    id:'01',
                    img_url:require("../../../assets/img/eggbeater.png"),
                    description:"攻略"
                },{
                    id:'01',
                    img_url:require("../../../assets/img/trash.png"),
                    description:"汽车票"
                },{
                    id:'01',
                    img_url:require("../../../assets/img/rolling.png"),
                    description:"国内游"
                },{
                    id:'01',
                    img_url:require("../../../assets/img/urn.png"),
                    description:"签证"
                }]
            }
        }

    }
</script>

<style scoped>
.box{
    display: flex;

    flex-wrap: wrap;
}
.img_box{
    width: 25%;
    text-align: center;
}
.img-content{
    width: 2rem;
    height: 2rem;
    margin-bottom: 0.5rem;
    margin-top: 1.1rem;
}
</style>