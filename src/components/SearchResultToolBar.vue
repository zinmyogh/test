<template>
    <div class="search-result-toolbar">
        <img @click="goHome" class="logo" src="./../assets/logo.png" alt="">
        <RoundSearchBar :search="search"/>
    </div>
</template>

<script>
import RoundSearchBar from "@/components/RoundSearchBar.vue";
export default {
    name: "search-result-toolbar",
    props: ['search'],
    components:{
        RoundSearchBar
    },
    methods: {
        goHome(){
            return this.$router.push('/')
        }
    }
}
</script>

<style lang="less" scoped>
@import "./../theme/base.less";

.search-result-toolbar{
    text-align: left;
    padding: @space-large;
    border-bottom: solid 1px @color-border-gray;
}
.logo{
    vertical-align: top;
    height: @round-search-bar-height*0.8;
    margin: @space-large;
}
</style>