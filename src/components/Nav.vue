<template>
    <nav>
        <router-link to="/money" class="item" active-class="selected">
            <Icon name="money"></Icon>
            首页
        </router-link>
        <router-link to="/labels" class="item" active-class="selected">
            <Icon name="label"></Icon>
            标签
        </router-link>
        <router-link to="/statistics" class="item" active-class="selected">
            <Icon name="statistics"></Icon>
            统计
        </router-link>
    </nav>
</template>

<script lang="ts">
    export default {
        name: 'Nav'
    };
</script>

<style lang="less" scoped>
    nav {
        display: flex;
        flex-direction: row;
        box-shadow: 0 0 3px rgba(0, 0, 0, 0.8);
        font-size: 12px;

        > .item {
            display: flex;
            flex-direction: column;
            width: 33.33333%;
            justify-content: center;
            align-items: center;
            padding: 2px 0;

            .icon {
                height: 32px;
                width: 32px;
            }
        }
    }

    .selected {
        color: #4fc08d;
    }

</style>