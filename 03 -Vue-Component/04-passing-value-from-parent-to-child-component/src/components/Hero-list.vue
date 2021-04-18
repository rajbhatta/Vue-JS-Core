<template>
    <div>
        <p>Property 1: {{titleChild}}</p>
        <p>Property 2: </p>
        <p>Property 3: </p>
        <p>Property 4: </p>
    </div>
</template>

<script>
    export default {
        name:'HeroList',
        props: {
            titleChild: String,
        },
    }
</script>

<style lang="scss" scoped>

</style>