<template lang="html">
    <div>
    <v-header/>
    <m-slider/>
    <ad-top/>
    <recommend/>
    <ad-middle/>
    <finance/>
    <ad-bottom  />
    <v-footer :cname="$style.footer"/>
    <navbar/>
    </div>
</template>

<script>
    import VHeader from '../common/Header'
    import VFooter from '../common/Footer'
    import MSlider from './MSlider'
    import AdTop from './adTop'
    import AdMiddle from './admiddle'
    import Recommend from './recommend'
    import Finance from './finance'
    import AdBottom from './adbottom.vue'
    import Navbar from '../common/Navbar'
export default {
    components:{
        VHeader,
        VFooter,
        MSlider,
        AdTop,
        Recommend,
        AdMiddle,
        Finance,
        AdBottom,
        Navbar,
    }
}
</script>

<style lang="scss" module>
    .footer{
        li:nth-child(1){
                display: none;
        }
    }
</style>
