<template>
    <panel title="新手特权" :cname="$style.npanel">
        <section :class="$style.content">
            <div :class="$style.item">
                <h4>下载APP<span :class="$style.red">送888元红包</span></h4>
                <p :class="$style.gray">新手专享</p>
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t10384/155/1759179594/9776/185bd062/59e5f0ebNec4cf494.png?width=100&height=100">
            </div>
            <div :class="$style.item">
                <ul>
                    <li>
                        <img src="//img12.360buyimg.com/jrpmobile/jfs/t4639/162/1782623297/60754/98ea03b4/58e60952N7fdb2b85.png?width=200&height=200"
                             alt="">
                        <h4 :class="$style.red">领128元新手礼包</h4>
                        <p :class="$style.gray">立即开通</p>
                    </li>
                    <li>
                        <img src="//img12.360buyimg.com/jrpmobile/jfs/t4804/179/657713323/5908/66dce262/58e6095fNd3dc3f39.png?width=100&height=100"
                             alt="">
                        <h4>打白条<span :class="$style.red">享免息</span></h4>
                        <p :class="$style.gray">立即开通享豪礼</p>
                    </li>
                </ul>
            </div>
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
    @import '../../css/element.scss';

    .npanel {
        > h4 {
            border-bottom: 1px solid #ddd;
        }
        .content {
            @include list(row);
            .item {
                flex: 1;
                text-align: center;
                &:first-child {
                    padding: 16px 10px;
                    border-right: 1px solid #ddd;
                    img {
                        width: 66px;
                        height: 66px;
                        margin: 10px auto 0;
                    }
                }
            }
            h4 {
                font-size: 13px;
                line-height: 40px;
            }
            .red {
                color: #f00;
            }
            .gray {
                color: #999;
                font-size: 12px;
            }
            ul {
                width: 100%;
                li {
                    overflow: hidden;
                    box-sizing: border-box;
                    text-align: left;
                    padding: 16px 14px;
                    width: 100%;
                    height: 77px;
                    &:first-child {
                        border-bottom: 1px solid #ddd;
                    }
                    h4 {
                        white-space: nowrap;
                        text-overflow: ellipsis;
                        overflow: hidden;
                        line-height: 2.2;
                    }
                    img {
                        float: right;
                        width: 40px;
                        height: 40px;
                    }
                }
            }
        }
    }
</style>
