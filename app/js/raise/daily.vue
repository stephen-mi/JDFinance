<template>
    <panel title="每日签到">
        <section :class="$style.content">
            <img src="//img12.360buyimg.com/jrpmobile/jfs/t3184/283/6032981290/37056/fa30c674/589bd5a2Nabdbbbd9.jpg?width=376&height=160"
                 alt="">
            <img src="//img12.360buyimg.com/jrpmobile/jfs/t3298/196/6130416421/33755/a0536d3e/589bd5d4Nf32e7adc.jpg?width=374&height=160"
                 alt="">
            <p>不抢白不抢</p>
        </section>
    </panel>
</template>

<script type="text/ecmascript-6">
    import Panel from '../common/Panel'

    export default {
        components: {
            Panel,
        }
    }
</script>

<style lang="scss" module>
    @import "../../css/element";

    .content {
        @include list(row);
        padding-bottom: 20px;
        position: relative;
        p{
            position: absolute;
            top:-56px;
            right: 10px;
            font-size: 14px;
            color: #999;
            line-height: 56px;
        }
    }
</style>