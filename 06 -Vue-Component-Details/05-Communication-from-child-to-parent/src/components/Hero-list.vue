<template>
    <div>
        <span>Hello from child component </span>
        <button type="button" v-on:click="saveHero()">Click</button>
    </div>
</template>

<script>

const OUR_HEROES=
        {
            id:10,
            firstName:"AF",
            lastName: "AL",
            description:"Test A"
        };

    export default {
        name:'HeroList',
        data() {
            return {
                theHero: OUR_HEROES
            }
        },
        methods: {
            saveHero() {
                this.$emit("saveHeroInParent",this.theHero)
            }
        },
    }
</script>

<style lang="scss" scoped>

</style>