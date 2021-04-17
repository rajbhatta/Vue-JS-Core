<template>
    <div>
        <Header></Header>
        <HeroAdd></HeroAdd>
        <HeroDetail></HeroDetail>
        <HeroList></HeroList>
    </div>
</template>

<script>
import Header from './Header.vue'
import HeroAdd from '@/components/Hero-add.vue'
import HeroDetail from './Hero-detail.vue'
import HeroList from './Hero-list.vue'

    export default {
        name:'Heros',
        components:{Header,HeroAdd,HeroDetail,HeroList}
    }
</script>

<style lang="scss" scoped>

</style>