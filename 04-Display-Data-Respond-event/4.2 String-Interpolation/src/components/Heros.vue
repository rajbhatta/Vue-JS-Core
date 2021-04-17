<template>
    <div>
        <Header></Header>
        <HeroDetail></HeroDetail>
        <HeroList></HeroList>
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