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
                    href: "ious",
                    src: "//img12.360buyimg.com/jrpmobile/jfs/t8491/303/504628479/60643/100648de/59a94358N92475fca.jpg?width=750&height=320",
                }, {
                    href: "home",
                    src: "//img12.360buyimg.com/jrpmobile/jfs/t8437/321/1758527686/40952/f66d552f/59bf1f41N50d846f9.jpg?width=750&height=320",
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
