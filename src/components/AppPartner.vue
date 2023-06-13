<script>
export default {
    name: "AppPartner",
}
</script>

<template>
    <section class="partner">
        <div>
            <a href="#">
                <img src="./../assets/img/amazon.svg" alt="amazon">
            </a>
            <a href="#">
                <img src="./../assets/img/google.svg" alt="google">
            </a>
            <a href="#">
                <img src="./../assets/img/lenovo.svg" alt="lenovo">
            </a>
            <a href="#">
                <img src="./../assets/img/paypal.svg" alt="paypal">
            </a>
            <a href="#">
                <img src="./../assets/img/shopify.svg" alt="shopify">
            </a>
            <a href="#">
                <img src="./../assets/img/spotify.svg" alt="spotify">
            </a>
        </div>
    </section>
</template>

<style scoped lang="scss">
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;

.partner {
    border-top: 1px solid rgb(235, 235, 235);

    div {
        width: 65%;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
        padding: 30px 0 20px;
    }

    img {
        width: 60px;
    }
}
</style>