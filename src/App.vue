<template>
    <div id="app">
        <router-view/>
    </div>
</template>

<style lang="less">
    @import "~@/assets/styles/reset.less";
    @import "~@/assets/styles/global.less";

    #app {
        line-height: 1.5;
        font-family: @font-hei;
        color: #333;
    }
</style>
