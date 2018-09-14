<template>
    <div class="icons">
        <swiper class="swipper" :options="swiperOption" >
            <swiper-slide >
                <div class="box">
                    <div class="img_box" v-for="i of list">
                        <img class="img-content" :src="i.img_url">
                        <p>{{i.description}}</p>
                    </div>
                </div>
            </swiper-slide>


            <swiper-slide >
                <div class="box">
                    <div class="img_box" v-for="i of list">
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
        props:{
            list:Array
        },
        data (){
            return{
                swiperOption: {
                    loop:true
                },
                iconList:[]
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