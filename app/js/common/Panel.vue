<template>
    <div :class="[panelClass,cname]">
        <h4 class="title">-{{title}}-</h4>
        <slot/>
    </div>
</template>

<script type="text/ecmascript-6">
    export default {
        props: {
            cname: {
                type: String,
                default: "",
            },
            title: {
                type: String,
                default: "",
            },
        },
        data() {
            return {
                panelClass: "panel",
            }
        },
    }
</script>

<style lang="scss">
    @import "../../css/element.scss";
    .panel {
        @include panel;
    }
</style>
