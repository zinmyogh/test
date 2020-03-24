<template>
  <div class="home">
    <MySearchLogo class="my-search-logo"/>
    <HomeSearchBar/>
  </div>
</template>

<script>
// @ is an alias to /src

import MySearchLogo from '@/components/MySearchLogo.vue'
import HomeSearchBar from '@/components/HomeSearchBar.vue'



export default {
  name: 'home',
  components: {
   HomeSearchBar,
    MySearchLogo
  }
}
</script>

<style lang="less" scoped>
 .my-search-logo{
   padding-top: 60px;
 }
</style>