<template>
    <panel title="白条福利" :cname="$style.panel">
        <ul :class="$style.content">
            <li :class="$style.item">
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t4378/62/155957680/9017/16463551/58affd58Nb5c9198e.jpg?width=120&height=120" alt="">
                <div>
                    <h4>开通白条</h4>
                    <p>送188元礼包</p>
                </div>
                <em>立即开通 > </em>
            </li>
            <li :class="$style.item">
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t4150/330/141981421/9147/604e3e04/58affc3bNbfa8f9d7.jpg?width=120&height=120" alt="">
                <div>
                    <h4>白条闪付</h4>
                    <p>新手享158元礼包</p>
                </div>
                <em>随机立减 > </em>
            </li>
            <li :class="$style.item">
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t4270/96/1102370053/8651/58b7fa5a/58bd2e10N453e9464.jpg?width=120&height=120" alt="">
                <div>
                    <h4>白条提额</h4>
                    <p>金融app专享提额礼包</p>
                </div>
                <em>去提额 > </em>
            </li>
        </ul>
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

    .panel {
        > h4 {
            border-bottom: 1px solid #ddd;
        }
        .content {
            .item {
                @include list(row);
                height: 70px;
                align-items: center;
                &::after {
                    content: "";
                    margin-left: 75px;
                    box-sizing: border-box;
                    height: 0;
                    width: 100%;
                    border-bottom: 1px solid #ddd;
                }
                &:last-child::after{
                    border-color: #fff;
                }
                img {
                    flex: 0 0 44px;
                    margin: 0 16px;
                    width: 44px;
                    height: 44px;
                }
                div {
                    flex: 1;
                    line-height: 1.8;
                    font-size: 16px;
                    color: #111;
                    font-weight: 700;
                    p {
                        line-height: 1.1;
                        color: #666;
                        font-size: 12px;
                        white-space: nowrap;
                        text-overflow: ellipsis;
                        overflow: hidden;
                    }
                }
                em {
                    flex: 0 0 75px;
                    color: #FF801A;
                    font-size: 14px;
                }
            }
        }
    }
</style>
