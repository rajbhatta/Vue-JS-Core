<template>

    <div>
        <Header></Header>
    </div>
    <div>
        <HeroDetail></HeroDetail>
    </div>
    <div>
        <HeroList @saveHeroInParent="getHeroObjFromChild"></HeroList> 
    </div>

    <h2>Value received from child </h2>
    {{hero.firstName}}
</template>

<script>
import Header from './Header.vue'
import HeroDetail from './Hero-detail.vue'
import HeroList from './Hero-list.vue'

    export default {
        name:'Heros',
        components:{Header,HeroDetail,HeroList},
        data() {
            return {
                hero: {}
            }
        },
        methods: {
            getHeroObjFromChild(passedValue) {
                this.hero=passedValue;
            }
        },
    }
</script>

<style lang="scss" scoped>

</style>