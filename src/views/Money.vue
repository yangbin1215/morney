<template>
    <div>
        <Layout class-prefix="layout">
            <NumberPad/>
            <Types/>
            <Notes/>
            <Tags/>
        </Layout>
    </div>
</template>

<script lang="ts">
    import NumberPad from '@/components/money/NumberPad.vue';
    import Types from '@/components/money/Types.vue';
    import Notes from '@/components/money/Notes.vue';
    import Tags from '@/components/money/Tags.vue';
    export default {
        name: 'Money',
        components: {Tags, Notes, Types, NumberPad}
    };
</script>

<style lang="less">
    .layout-content {
        display: flex;
        flex-direction: column-reverse;
    }
</style>