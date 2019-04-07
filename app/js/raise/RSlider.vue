<template>
    <div :class="$style.sliderWrppaer">
        <swiper :options="options">
            <swiper-slide>百万白条券免费送，速来领取！！ <em>></em></swiper-slide>
            <swiper-slide>签到领流量，1元500M！<em>></em></swiper-slide>
        </swiper>
    </div>
</template>

<script type="text/ecmascript-6">
    import {swiper, swiperSlide} from 'vue-awesome-swiper'

    export default {
        data() {
            return {
                options: {
                    autoplay: true,
                    loop: true,
                    direction: 'vertical'
                },
            }
        },
        components: {
            swiper,
            swiperSlide
        }
    }
</script>

<style lang="scss">
    .swiper-container-vertical {
        .swiper-slider {
            font-family: PingFangSC-Medium;
            font-size: 14px;
            color: #333;
        }
        em {
            color: #ddd;
            float: right;
            margin-right: 10px;
        }
    }
</style>

<style lang="scss" module>
    @import "../../css/element";

    .slider-wrppaer {
        margin-top: 60px;
        line-height: 36px;
        height: 36px;
        overflow: hidden;
        padding-left: 90px;
        background: #fff url(//m.jr.jd.com/spe/qyy/main/images/scroll_title_img.png) left top no-repeat;
    }
</style>
