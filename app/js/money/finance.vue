<template>
    <panel title="理财精选" :cname="$style.panel">
        <ul :class="$style.content">
            <li :class="$style.item">
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t3670/58/543125556/2606/a65096b9/580d80afN63b1085a.png?width=76&height=76"
                     alt="">
                <div>
                    <h4>月度理财</h4>
                    <p>预期年化收益率4.50%</p>
                </div>
                <em>去赚钱 > </em>
            </li>
            <li :class="$style.item">
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t3679/44/511862277/2728/c1c6b2bf/580d8189N6b6f8052.png?width=76&height=76"
                     alt="">
                <div>
                    <h4>季度理财</h4>
                    <p>历史年化回报率5.50%</p>
                </div>
                <em>去赚钱 > </em>
            </li>
            <li :class="$style.item">
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t3331/69/580199498/3074/d5bb21c5/580d7f6cN7f35e596.png?width=76&height=76"
                     alt="">
                <div>
                    <h4>一年理财</h4>
                    <p>历史年化回报率5.80%</p>
                </div>
                <em>去赚钱 > </em>
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
                    color: #333;
                    p {
                        line-height: 1.1;
                        color: #ff3232;
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
