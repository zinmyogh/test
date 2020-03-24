<template>
    <div class="container">
        <input v-model="searchText" class="input-search" @keydown.enter="doSearch">
        <button class="btn-search" @click="doSearch">Search</button>
    </div>
</template>

<script>
import util from '@/common/util'
export default {
    name: "home-search-bar",
    data() {
        return {
            searchText: ""
        }
    },
    methods: {
        doSearch() {
            util.searchAPI(this.$router, this.searchText.toLowerCase())
            }
        }
    }

</script>

<style lang="less" scoped>
@import "./../theme/base.less";
  .container{
      margin-top: 50px;
      margin-right: 100px;
      margin-left: 100px;
  }
    .input-search{
        outline: none;
        width: 300px;
        border-radius: 10px;
        margin-right: 20px;    
         height: @home-search-bar;
         box-sizing: border-box;
         border: 1px solid @color-border-gray;
         padding: 15px;
    }
    .btn-search{
        outline: none;
        border-radius: 10px;
        width: 100px;
         height: @home-search-bar;
         box-sizing: border-box;
         background-color: @color-primary;
         color: silver;
         border: none;
    }
</style>