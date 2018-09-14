<template>
    <div>
        <swiper class="swipper" :options="swiperOption" >
            <swiper-slide v-for="item of list" >
                <img :src="item.img_url" />
            </swiper-slide>
            <!-- Optional controls -->
            <div class="swiper-pagination"  slot="pagination"></div>
        </swiper>
    </div>
</template>

<script>
    export default {
        props:{
            list:Array
        },
        data (){
            return{
                swiperOption: {
                    pagination: {
                        el: '.swiper-pagination'
                    },
                    loop:true
                }

            }
        }
        // name: "swiper",
        // data() {
        //     return {
        //         swiperOption: {
        //
        //         }
        //     }
        // },
        // computed: {
        //     swiper() {
        //         return this.$refs.mySwiper.swiper
        //     }
        // },
        // mounted() {
        //     current swiper instance
        //     然后你就可以使用当前上下文内的swiper对象去做你想做的事了
        //
        // }
    }
</script>

<style scoped>
    /*穿透*/
    .swipper >>> .swiper-pagination-bullet-active {
        background-color:#fff
    }

.swipper{
    height: 8.5rem;
}
    img{
        width: 100%;
        height: 100%;

    }
</style>