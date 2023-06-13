<script>
import AppNavBar from "./AppNavBar.vue"
import AppJumbotron from "./AppJumbotron.vue"
import AppPartner from "./AppPartner.vue";

export default {
    name: "PageHeader",
    components: {
        AppNavBar,
        AppJumbotron,
        AppPartner,
    },
    props: {
        vociMenuHeader: Array
    }
}
</script>

<template>
    <div class="container">
        <div class="setting">
            <a href="#">
                <i class="fa-solid fa-gear"></i>
            </a>
        </div>

        <AppNavBar :vociMenuHeaderOnPageHeader="vociMenuHeader" />
        <AppJumbotron />
        <AppPartner />
    </div>
</template>

<style scoped lang="scss">
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;

.container {
    background-color: #f8f9fc;
    width: 100%;
    padding: 10px 0;
    position: relative;
}

.setting {
    position: absolute;
    left: -10px;
    top: 100px;
    background-color: white;
    padding: 5px 5px 5px 15px;
    border-radius: 15px;

    a {
        color: $colore_primario;
    }
}
</style>
