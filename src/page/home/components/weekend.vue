<template>
    <div>
        <div class="title">周末去哪儿</div>
        <ul>
            <li class="item" v-for="(i,k) of itemList" :key="k">
                <div class="img_wrapper">
                    <img class="item_img" :src="i.img_url" >
                </div>
                <div class="info">
                    <p class="item_title">{{i.title}}</p>
                    <p class="des">{{i.des}}</p>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
    export default {
        name: "weekend",
        methods:{

        },
        data(){
            return{
                itemList:[{
                    img_url:require("../../../assets/img/sea1.jpg"),
                    title:"温泉有水上乐园",
                    des:"泡泡温泉，吹吹海风，神诀人生美好",
                },{
                    img_url:require("../../../assets/img/sea2.jpg"),
                    title:"大连成员温泉",
                    des:"与动物嬉戏，共享和谐人生与动物嬉戏与动物嬉戏",
                },{
                    img_url:require("../../../assets/img/sea3.jpg"),
                    title:"老虎滩海燕公园",
                    des:"浓缩极低世界，展现海洋奇怪",
                },{
                    img_url:require("../../../assets/img/sea4.jpg"),
                    title:"大连香洲旅游度假区",
                    des:"将壮观诠释到完美，将梦想展示给世界",
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
        padding: 5px;
    }
    .item{
        display: flex;
        flex-direction: column;
    }
    .img_wrapper{
    }
    .item_img{
        width: 100%;
        height: 8rem;
    }
    .item_title{
        font-size: 0.9rem;
        font-weight: bold;
    }
    .info{
        /*设置文字超出后出现省略号需加入 min-width：0*/
        min-width: 0;
        padding: 1rem;
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