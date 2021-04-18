<template>
    <div>
        <Header></Header>
    </div>
    <div>
        <HeroDetail></HeroDetail>
    </div>
    <div>
        <HeroList :heroObject="heros"></HeroList>  // Note that prepending a colon to the prop attribute indicates that a variable is passed, not a string.
    </div>
</template>

<script>
import Header from './Header.vue'
import HeroDetail from './Hero-detail.vue'
import HeroList from './Hero-list.vue'

const OUR_HEROES=
        {
            id:10,
            firstName:"AF",
            lastName: "AL",
            description:"Test A"
        };

    export default {
        name:'Heros',
        components:{Header,HeroDetail,HeroList},
        data() {
            return {
                heros: OUR_HEROES
            }
        },
    }
</script>

<style lang="scss" scoped>

</style>