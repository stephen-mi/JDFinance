<template lang="html">
    <div>
    <v-header/>
    <r-slider/>
    <daily/>
    <in/>
    <more/>
    <v-footer :cname="$style.footer"/>
    <navbar/>
    </div>
</template>

<script>
    import VHeader from '../common/Header'
    import VFooter from '../common/Footer'
    import RSlider from './RSlider'
    import Daily from './daily'
    import In from './in'
    import Navbar from '../common/Navbar'
    import More from './more'
 export default {
    components:{
        VHeader,
        VFooter,
        RSlider,
        Daily,
        In,
        More,
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
