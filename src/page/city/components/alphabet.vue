<template>
    <ul class="list">
        <li class="item" v-for="(i,k) of alphabetList">{{k}}</li>
    </ul>
</template>

<script>
    export default {
        name: "alphabet",
        props:['alphabetList']
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
        line-height: 1.5rem;
        color: deepskyblue;
    }
</style>