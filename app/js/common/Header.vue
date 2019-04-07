<template>
    <header :class="$style.header">
        <div :class="$style.left">
            <span>登录</span>|<span>注册</span>
        </div>
        <div :class="$style.right">
            <button :class="[$style.cbtn,'btn']">下載APP</button>
        </div>
    </header>
</template>

<script type="text/ecmascript-6">
    export default {}
</script>

<style lang="scss" module>
    .header {
        position: fixed;
        top: 0;
        left: 0;
        right: 0;
        height: 50px;
        line-height: 50px;
        font-size: 16px;
        color: #666;
        background: #fff url(//m.jr.jd.com/spe/qyy/main/images/jr-logo.png) center center no-repeat;
        background-size: auto 50%;
        z-index: 100;
        overflow: hidden;
        .left {
            float: left;
            margin: 8px 0 0 9px;
            line-height: 30px;
            height: 30px;
            font-size: 14px;
        }
        .right {
            float: right;
            .cbtn {
                margin: 14px 12px 0 0;
                padding: 0;
                font-size: 12px;
                border-width: 0;
                height: 28px;
                line-height: 28px;
                min-width: 60px;
                border-radius: 2px;
            }
        }
    }
</style>
