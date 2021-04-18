<template>
    <div>
        <h3>{{heroTitle}}</h3>
        <h4> Hero First Name: {{hero.firstName}} </h4>
        <h4> Hero Last Name: {{hero.lastName}} </h4>
        <h4> Hero id: {{hero.id}} </h4>
    </div>
</template>

<script>
    export default {
        name:'HeroDetail',
        data() {
            return {
                heroTitle: "This is hero details",
                hero:{
                    id:20,
                    firstName:"Raj",
                    lastName:"Bhatta"
                }
            }
        },
    }
</script>

<style lang="scss" scoped>

</style>