<template>
    <div :class="$style.sliderWrppaer">
        <slider :items="items" :cname="$style.slider"></slider>
        <div :class="$style.list">
            <div :class="$style.item" v-for="item in enters" :key="item.href">
                <router-link :to="item.href">
                    <img :src="item.img" :alt="item.title">
                    <h4 :class="$style.title">{{item.title}}</h4>
                </router-link>
            </div>
        </div>
    </div>
</template>

<script type="text/ecmascript-6">
    import Slider from '../common/slider'

    export default {
        data() {
            return {
                items: [
                    {
                        href: "home",
                        src: "//img12.360buyimg.com/jrpmobile/jfs/t13744/11/2508939408/43213/58bfe502/5a421ff3N52d0a474.jpg?width=750&height=320",
                    }, {
                        href: "home",
                        src: "//img12.360buyimg.com/jrpmobile/jfs/t16138/325/817844900/36681/5d874455/5a422029Ncd678ea3.jpg?width=750&height=320",
                    }, {
                        href: "home",
                        src: "//img12.360buyimg.com/jrpmobile/jfs/t13465/324/2563794460/43029/3ffca963/5a421f83Ne8089231.jpg?width=750&height=320",
                    }],
                enters: [
                    {
                        href: "download",
                        img: "//img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png?width=132&height=132",
                        title: "优惠券",
                    }, {
                        href: "home",
                        img: "//img12.360buyimg.com/jrpmobile/jfs/t5590/252/875247023/17343/946aa72c/59224650N0f7ffc92.png?width=132&height=132",
                        title: "领红包",
                    }, {
                        href: "home",
                        img: "//img12.360buyimg.com/jrpmobile/jfs/t4618/115/2179710654/11347/bf520df/58ec9d84Nfd169001.png?width=132&height=132",
                        title: "领京豆",
                    }, {
                        href: "home",
                        img: "//img12.360buyimg.com/jrpmobile/jfs/t5488/298/1036263348/12073/b4f4de97/590ac8e8Ne9def22e.png?width=135&height=135",
                        title: "白条提额",
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
