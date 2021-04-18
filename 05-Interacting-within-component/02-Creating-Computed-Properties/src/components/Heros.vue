<template>
    <div>
        <Header></Header>
        <HeroList></HeroList>
    </div>
</template>

<script>
import Header from './Header.vue'
import HeroList from './Hero-list.vue'

    export default {
        name:'Heros',
        components:{Header,HeroList}
    }
</script>

<style lang="scss" scoped>

</style>