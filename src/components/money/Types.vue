<template>
    <ul class="types">
        <li class="selected">支出</li>
        <li>收入</li>
    </ul>
</template>

<script lang="ts">
    export default {
        name: 'Types'
    };
</script>

<style lang="less" scoped>
    @import "~@/assets/styles/global.less";

    .types {
        background: #c4c4c4;
        font-size: 24px;
        display: flex;
        text-align: center;

        > li {
            width: 50%;
            height: 64px;
            display: flex;
            justify-content: center;
            align-items: center;
            position: relative;

            &.selected::after {
                content: '';
                position: absolute;
                bottom: 0;
                left: 0;
                width: 100%;
                height: 4px;
                background: @vue-color;
            }
        }
    }
</style>