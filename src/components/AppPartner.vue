<script>
export default {
    name: "AppPartner",
    data() {
        return {
            partners: [
                {
                    name: "amazon",
                    url: "#",
                    src: "./src/assets/img/amazon.svg"
                },
                {
                    name: "google",
                    url: "#",
                    src: "./src/assets/img/google.svg"
                },
                {
                    name: "lenovo",
                    url: "#",
                    src: "./src/assets/img/lenovo.svg"
                },
                {
                    name: "paypal",
                    url: "#",
                    src: "./src/assets/img/paypal.svg"
                },
                {
                    name: "shopify",
                    url: "#",
                    src: "./src/assets/img/shopify.svg"
                },
                {
                    name: "spotify",
                    url: "#",
                    src: "./src/assets/img/spotify.svg"
                },
            ]
        }
    }
}
</script>

<template>
    <section class="partner">
        <div>
            <a v-for="(partner, index) in partners" :href="partner.url" :key="index">
                <img :src="partner.src" :alt="partner.name">
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