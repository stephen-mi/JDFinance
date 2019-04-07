<template lang="html">
    <div>
    <v-header/>
    <i-slider/>
    <welfare/>
    <service/>
    <v-footer :cname="$style.footer"/>
    <navbar/>
    </div>
</template>

<script>
    import VHeader from '../common/Header'
    import VFooter from '../common/Footer'
    import ISlider from './ISlider'
    import Welfare from './welfare'
    import Service from './service'
    import Navbar from '../common/Navbar'
export default {
    components:{
        VHeader,
        VFooter,
        ISlider,
        Welfare,
        Service,
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
