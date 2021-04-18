<template>
    <div>
        <Header></Header>
    </div>
    <div>
        <HeroDetail></HeroDetail>
    </div>
    <div>
        <HeroList titleChild="This title is for child sent from parent"></HeroList>
    </div>
</template>

<script>
import Header from './Header.vue'
import HeroDetail from './Hero-detail.vue'
import HeroList from './Hero-list.vue'

    export default {
        name:'Heros',
        components:{Header,HeroDetail,HeroList}
    }
</script>

<style lang="scss" scoped>

</style>