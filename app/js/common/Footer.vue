<template>
    <panel title="公司信息" :class="cname" :cname="$style.panel">
        <ul :class="$style.content">
            <li>
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t2842/350/3035567089/14791/5f6ff93d/577cf395N31e76288.png?width=1125&height=252"
                     alt="">
            </li>
            <li>
                <div>
                    <img src="//img12.360buyimg.com/jrpmobile/jfs/t2971/333/1297567079/898/f2d2e00d/577dc28dNe5138337.png?width=108&height=108"
                         alt="">
                    <p>客户端</p>
                </div>
                <div>
                    <img src="//img12.360buyimg.com/jrpmobile/jfs/t2824/256/2966087355/831/188bfa25/577cf3dcN18aadbf2.png?width=108&height=108"
                         alt="">
                    <p>触屏版</p>
                </div>
                <div>
                    <img src="//img12.360buyimg.com/jrpmobile/jfs/t2920/282/1283157010/1040/23f1430b/577cf3e5N53f740b8.png?width=108&height=108"
                         alt="">
                    <p>电脑版</p>
                </div>
            </li>
            <li>Copyright © 2004-2017 京东JD.com 版权所有</li>
            <li>投资有风险，购买需谨慎</li>
            <li>京东金融平台服务协议</li>
            <li>京东金融隐私政策</li>
        </ul>
    </panel>
</template>

<script type="text/ecmascript-6">
    import Panel from './Panel'

    export default {
        props: {
            cname: String
        },
        components: {
            Panel,
        }
    }
</script>

<style lang="scss" module>
    @import "../../css/element";

    .panel {
        margin-bottom: 50px;
        > h4 {
            display: none;
        }
        .content {
            background: #f5f5f5;
            li {
                text-align: center;
                color: #999;
                font-size: 12px;
                > img {
                    width: 100%;
                }
                &:nth-child(2) {
                    @include list(row);
                    box-sizing: border-box;
                    padding-top: 10px;
                    height: 93px;
                    div {
                        width: 33.33%;
                        img {
                            width: 45px;
                            height: 45px;
                        }
                        p {
                            margin-top: 6px;
                            font-size: 13px;
                            white-space: nowrap;
                            text-overflow: ellipsis;
                            overflow: hidden;
                        }

                    }
                }
                &:nth-child(n+3) {
                    padding: 12px 0;
                    line-height: 19px;
                    border-top: 1px solid #ddd;
                }
            }
        }
    }
</style>
