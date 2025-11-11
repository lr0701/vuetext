<template>
    <div class="zujianshijianModel">
        <h3>组件自定义事件+model</h3>
        <p>搜索内容：{{ search }}</p>
        <zujianshijianModelSearch @searchText="getSearch"></zujianshijianModelSearch>
    </div>
</template>

<script>
import zujianshijianModelSearch from '../pages/zujianshijianVmodelSearch.vue';
export default {
    name: "zujianshijianModel",
    data() {
        return {
        search: ''
        }
    },
    components: {
        zujianshijianModelSearch
    },
    methods: {
        getSearch(data) {
        this.search = data;
        console.log(data, '+++++++++++++++');
        }
    }
}
</script>

<style scoped>
.zujianshijianModel {
    color: green;
}
</style>