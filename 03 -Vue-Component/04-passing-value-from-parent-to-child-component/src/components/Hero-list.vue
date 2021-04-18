<template>
    <div>
        <p>Property 1: {{heroObject.id}}</p>
        <p>Property 2: {{heroObject.firstName}} </p>
        <p>Property 3: {{heroObject.lastName}}</p>
        <p>Property 4: {{heroObject.description}}</p>
    </div>
</template>

<script>
    export default {
        name:'HeroList',
        props: {
            heroObject: Object,
        },
    }
</script>

<style lang="scss" scoped>

</style>