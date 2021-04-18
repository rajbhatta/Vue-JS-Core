<template>
    <div>
        <h3>This is hero details</h3>
    </div>
</template>

<script>
    export default {
        name:'HeroDetail',
        props: {
            hero: {
                type: Object,
                default: () => {}
            },
        },
    };
</script>

<style lang="scss" scoped>

</style>