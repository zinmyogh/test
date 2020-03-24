<template>
    <div class="search-result-item" :href="info.url">
     <a class="result-a" :href="info.url">
        <div class="title">{{ info.title }}</div>
        <div class="url">{{ info.url }}</div>
        <div class="desc">{{ info.date }} -- {{ info.desc }}</div>
     </a>
    </div>
</template>

<script>
export default {
    props: ["info"]
}
</script>

<style lang="less" scoped>
    .search-result-item{
        // border: solid 1px silver;
        text-align: left;
        padding: 20px;
    }
    .result-a{
        text-decoration: none;
    }
    .title{
        color: #190DAA;
        font-size: 1.2em;
    }
    .url{
        color: green;
        font-weight: bold;
    }
    .desc{
        color: gray;
    }
</style>