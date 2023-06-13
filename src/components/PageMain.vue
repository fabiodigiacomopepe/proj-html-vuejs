<script>
import AppKeyFeatures from './AppKeyFeatures.vue';
import AppQuickStart from './AppQuickStart.vue';
import AppBuildTools from './AppBuildTools.vue';
import AppPrice from './AppPrice.vue';
import AppGetStarted from './AppGetStarted.vue';

export default {
    name: "PageMain",
    components: {
        AppKeyFeatures,
        AppQuickStart,
        AppBuildTools,
        AppPrice,
        AppGetStarted
    }
}
</script>

<template>
    <div class="container">
        <AppKeyFeatures />
        <AppQuickStart />
        <AppBuildTools />
        <AppPrice />
        <AppGetStarted />
    </div>
</template>

<style scoped lang="scss">
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;

.container {
    width: 70%;
    margin: 0 auto;
    margin-top: 70px;
}
</style>
