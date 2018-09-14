<template>
    <div>
        <div class="title">热销推荐</div>
        <ul>
            <li class="item" v-for="(i,k) of itemList" :key="k">
                <div class="img_wrapper">
                    <img class="item_img" :src="i.img_url" >
                </div>
                <div class="info">
                    <p class="item_title">{{i.title}}</p>
                    <p class="des">{{i.des}}</p>
                    <p class="price_box"><span>￥</span><span class="price">{{i.price}}&nbsp;</span>起</p>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
    export default {
        name: "recommend",
        methods:{

        },
        data(){
            return{
                itemList:[{
                    img_url:require("../../../assets/img/sanya.jpg"),
                    title:"大连圣亚海洋世界",
                    des:"浪漫大连首战，浪漫的海洋主题乐园",
                    price:99
                },{
                    img_url:require("../../../assets/img/euro.jpg"),
                    title:"大连成员温泉",
                    des:"与动物嬉戏，共享和谐人生与动物嬉戏与动物嬉戏",
                    price:48
                },{
                    img_url:require("../../../assets/img/Japan.jpg"),
                    title:"老虎滩海燕公园",
                    des:"浓缩极低世界，展现海洋奇怪",
                    price:50
                },{
                    img_url:require("../../../assets/img/lijiang.jpg"),
                    title:"大连香洲旅游度假区",
                    des:"将壮观诠释到完美，将梦想展示给世界",
                    price:10
                },{
                    img_url:require("../../../assets/img/bali.jpg"),
                    title:"大连森林动物园",
                    des:"有温泉，有嬉水乐园",
                    price:20
                }]
            }
        }
    }
</script>

<style scoped>
.title{
    background: #eee;
    line-height: 1.8rem;
    margin-top: 0.5rem;
    font-size: 0.8rem;
    text-indent: 0.5rem;
}
.item{
    display: flex;
    padding: 10px;
    border-bottom: 1px solid #eee;
}
.img_wrapper{
    margin-right: .5rem;
}
.item_img{
    width: 6rem;
}
.item_title{
    font-size: 0.9rem;
    font-weight: bold;
}
.info{
    /*设置文字超出后出现省略号需加入 min-width：0*/
    min-width: 0;
}
.des{
    color: #888;
    font-size: 0.9rem;
    font-family: "Microsoft YaHei UI";
    margin-top: 0.3rem;
    /*设置文字超出后出现省略号*/

    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
}
.price_box{
    font-size: 0.8rem;
    color:#888;
}
.price{
    font-size: 1.5rem;
    color: orange;

}
</style>