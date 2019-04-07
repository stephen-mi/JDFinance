<template>
    <panel title="理财精选">
        <section :class="$style.content">
            <dl :class="$style.item" v-for="item in items" :key="item.title">
                <dt>{{item.title}}<span>{{item.sub}}</span></dt>
                <dd>{{item.rate}}</dd>
                <dd>{{item.text}}</dd>
            </dl>
        </section>
    </panel>
</template>

<script type="text/ecmascript-6">
    import Panel from '../common/Panel'

    export default {
        data() {
            return {
                items: [{
                    title: "定期理财",
                    sub: "理财首选",
                    rate: "5.60%",
                    text: "历史年化回报率",
                }, {
                    title: "小白理财",
                    sub: "理财首选",
                    rate: "4.22%",
                    text: "7日年化收益率",
                }, {
                    title: "月月盈",
                    sub: "养老保障",
                    rate: "5%",
                    text: "七日年化收益率",
                }, {
                    title: "小白基金",
                    sub: "天天赚钱",
                    rate: "4.27%",
                    text: "7日年化收益率",
                }],
            }
        },
        components: {
            Panel
        }
    }
</script>

<style lang="scss" module>

    @import "../../css/element";

    .content {
        @include list(row);
        &::after {
            content: "";
            position: relative;
            top: -104px;
            display: block;
            width: 100%;
            height: 0;
            border-bottom: 1px solid #eee;
        }
        .item {
            position: relative;
            box-sizing: border-box;
            padding: 17px 20px;
            width: 50%;
            dt {
                font-size: 15px;
                line-height: 21px;
                color: #333;
                span {
                    margin-left: 2px;
                    padding: 0 8px;
                    vertical-align: 1px;
                    font-size: 11px;
                    color: #ff5155;
                    border: 1px solid #ff5155;
                }
            }
            dd {
                white-space: nowrap;
                text-overflow: ellipsis;
                overflow: hidden;
                &:nth-child(2) {
                    height: 29px;
                    line-height: 29px;
                    font-weight: 700;
                    font-size: 22px;
                    color: #FF5155;
                }
                &:nth-child(3) {
                    font-size: 12px;
                    height: 17px;
                    line-height: 17px;
                    color: #999;
                }
            }
            &::after {
                content: "";
                position: absolute;
                top: 50%;
                right: 0;
                margin-top: -34px;
                display: block;
                width: 1px;
                height: 68px;
                border-right: 1px solid #eee;
            }
            &:nth-child(2n) {
                &:after {
                    display: none;
                }
            }
        }
    }
</style>
