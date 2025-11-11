<template>
    <div class="zujianshijianModelSearch">
        搜索内容：<input type="text" v-model="searchText">
    </div>
</template>

<script>
export default {
    name: "zujianshijianModelSearch",
    data() {
        return {
        searchText: ''
        }
    },
    watch: {
        searchText(newValue, oldValue) {
        console.log(newValue, '+++++++++++++');
        console.log(oldValue, '------------');
        this.$emit('searchText', newValue);
        }
    }
}
</script>