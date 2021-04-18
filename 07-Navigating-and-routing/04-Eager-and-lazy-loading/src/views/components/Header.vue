<template>
    <div>
        <a :href="github">This is GitHubLink </a>
        <a v-bind:href="twitter">This is Twitter </a>
    </div>
</template>

<script>
    export default {
        name:'Header',
        data() {
            return {
                github: "http://github.com",
                twitter:"http://twitter.com"
            }
        },
    }
</script>

<style lang="scss" scoped>

</style>