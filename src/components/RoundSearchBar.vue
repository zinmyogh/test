<template>
    <div class="round-search-bar">
        <input v-model="search" class="input-search" @keydown.enter="doSearch"> <!-- onkeyup="this.value=this.value.toLowerCase()" -->
        <button class="btn-search" @click="doSearch">
            <img class="icon-search"  src="./../assets/logo.png" alt="">
        </button>
    </div>
</template>

<script>
import util from '@/common/util'

export default {
    name: "round-search-bar",
    props: ['search'],
    methods:{
        doSearch(){
            util.searchAPI(this.$router, this.search.toLowerCase())
        }
    } 
}
</script>

<style lang="less" scoped>
@import "./../theme/base.less";

.round-search-bar{
    position: relative;
    width: 400px;
    display: inline-block;
} 
.input-search{
    position: absolute;
    outline: none;
    width: 100%;
    height: @round-search-bar-height;
    border-radius: @round-search-bar-border-radius;
    border: solid 1px @color-border-gray;
    padding: 20px;
    box-sizing: border-box;
    font-size: 1.2em;
    display: inline-block;
}
.btn-search{
    height: @round-search-bar-height;
    position: absolute;
    right: 0px;
    top: 50%;
    transform: translateY(50%);
    background: none;
    border: none;
    outline: none;
}
.icon-search{
    bottom: 15px;
    position: relative;
    margin-right: 10px !important;
    width: 20px;
    height: 20px;
}
</style>