<template>
    <panel title="极速借贷">
        <section :class="$style.content">
            <router-link to="/home">
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t12721/42/2497849749/26333/ec584be4/5a421756N2416c88f.png?width=750&height=280"
                     alt="">
            </router-link>
        </section>
    </panel>
</template>

<script type="text/ecmascript-6">
    import Panel from '../common/Panel'

    export default {
        components: {
            Panel
        }
    }
</script>

<style lang="scss" module>
    .content {
        img {
            width: 100%;
        }
    }
</style>
