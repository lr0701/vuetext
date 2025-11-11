<template>
    <div class="zujianshuanzhipropp">
        <hr>
        <h3>父组件传值给子组件 props</h3>
        <Child :message="message" :age="age" :names="names" :userInfo="userInfo"></Child>
        <!-- <hr -->
        <hr>
    </div>
</template>

<script>
import Child from '../pages/child.vue';
export default {
    name: 'zujianshuanzhiprops',
    data() {
        return {
        message: '父组件传值给子组件',
        age: 18,
        names: ['张三', '李四', '王五'],
        userInfo: {
            title: '78978978989',
            id: 4545
        }
        };
    },
    components: {
        Child
    }
};
</script>

<style scoped>
.zujianshuanzhiprops {
    color: yellow;
}
</style>