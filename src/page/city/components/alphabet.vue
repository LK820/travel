<template>
    <ul class="list">
        <li @click="letterClick" @touchstart="touchStart" @touchmove="touchMove" @touchEnd="touchEnd" class="item" v-for="i of letters" :ref="i" :key="i">{{i}}</li>
    </ul>
</template>

<script>
    export default {
        name: "alphabet",
        props:{
            alphabetList:Object
        },
        data(){
            return {
                touchStatus:false,
                cities:this.alphabetList,
                startY:0,
                timer:null
            }
        },
        updated(){
            this.startY = this.$refs['A'][0].offsetTop
        },
        computed:{
            letters(){
                const letters = []
                for(let i in this.alphabetList){
                    letters.push(i)
                }
                return letters
            }

        },
        methods:{
            letterClick(e){
                this.$emit('change',e.target.innerText);
            },
            touchStart(){
                this.touchStatus = true
            },
            touchMove(e){
                if(this.touchStatus){
                    if(this.timmer){
                        clearTimeout(this.timer)
                    }else{
                        this.timer = setTimeout(()=>{
                            const touchY = e.touches[0].clientY - 72
                            const index = Math.floor((touchY-this.startY)/19.2)
                            if(index>=0&&index<this.letters.length){
                                this.$emit('change',this.letters[index])
                            }
                        },16)
                    }

                }
            },
            touchEnd(){
                this.touchStatus = false

            }
        }
    }
</script>

<style scoped>
    *{
        list-style: none;
    }
    .list{
        position: absolute;
        right: 0;
        top: 4rem;
        bottom: 0;
        display: flex;
        width: 1rem;
        flex-direction: column;
        justify-content: center;
    }
    .item{
        text-align: center;
        line-height: 1.2rem;
        font-size: 0.8rem;
        color: deepskyblue;
        font-family: "Microsoft YaHei UI";
    }
</style>