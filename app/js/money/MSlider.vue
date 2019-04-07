<template>
    <div :class="$style.sliderWrppaer">
        <slider :items="items" :cname="$style.slider"></slider>
    </div>
</template>

<script type="text/ecmascript-6">
    import Slider from '../common/slider'

    export default {
        data() {
            return {
                items: [{
                    href: "home",
                    src: "//img12.360buyimg.com/jrpmobile/jfs/t11149/181/856008463/68797/dc303e9/59f97baeN3cdae084.jpg?width=750&height=400",
                }, {
                    href: "home",
                    src: "//img12.360buyimg.com/jrpmobile/jfs/t9994/205/2575467053/189117/125e7b05/59f97c36N7599be57.png?width=750&height=400",
                }],
            }
        },
        components: {
            Slider
        }
    }
</script>

<style lang="scss" module>
    @import "../../css/element";

    .slider-wrppaer {
        .slider {
            margin-top: 50px;
            img {
                width: 100%;
            }
        }
        .list {
            @include list(row);
            justify-content: space-around;
            background: #fff;
            padding-top: 20px;
            padding-bottom: 10px;
            a {
                text-decoration: none;
            }
            .item {
                img {
                    display: block;
                    width: 45px;
                    height: 45px;
                }
                .title {
                    margin-top: 8px;
                    font-size: 14px;
                    color: #666;
                }
            }
        }
    }
</style>
