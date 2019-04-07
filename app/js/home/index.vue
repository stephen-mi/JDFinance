<template lang="html">
    <div>
        <v-header/>
        <v-slider/>
        <novice/>
        <borrow/>
        <money/>
        <product/>
        <life/>
        <v-footer/>
        <navbar/>
    </div>
</template>

<script>
    import VHeader from '../common/Header'
    import VFooter from '../common/Footer'
    import Navbar from '../common/Navbar'
    import VSlider from './VSlider'
    import Novice from './novice'
    import Borrow from './borrow'
    import Money from './money'
    import Product from './product'
    import Life from './life'
export default {
    components:{
        VHeader,
        VSlider,
        Novice,
        Borrow,
        Money,
        Product,
        Life,
        VFooter,
        Navbar,
    }
}
</script>

<style lang="scss" module>
</style>
