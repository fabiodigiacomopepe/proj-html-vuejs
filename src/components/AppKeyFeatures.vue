<script>
export default {
    name: "AppKeyFeatures",
    data() {
        return {
            hover: "",
            cards: [
                {
                    icon: "fa-solid fa-layer-group",
                    name: "Modular",
                    description: "Composed in a pseudo-Latin language which more or less corresponds.",
                    url: "#"
                },
                {
                    icon: "fa-solid fa-display",
                    name: "Responsive",
                    description: "Composed in a pseudo-Latin language which more or less corresponds.",
                    url: "#"
                },
                {
                    icon: "fa-solid fa-location-crosshairs",
                    name: "Customizable",
                    description: "Composed in a pseudo-Latin language which more or less corresponds.",
                    url: "#"
                },
                {
                    icon: "fa-solid fa-maximize",
                    name: "Scalable",
                    description: "Composed in a pseudo-Latin language which more or less corresponds.",
                    url: "#"
                },
            ]
        }
    }
}
</script>

<template>
    <section class="key_features">
        <div class="title_description">
            <h3>Key Features</h3>
            <div>Start working with <a href="#">Landrick</a> that can provide everything you need to generate awareness,
                drive
                traffic, connect.</div>
        </div>

        <div class="card_container">
            <div v-for="(card, index) in cards" :key="index" class="single_card" @mouseover="hover = index + 1"
                @mouseleave="hover = 0">
                <i :class="`${card.icon} icone`"></i>
                <h5>{{ card.name }}</h5>
                <div class="description">{{ card.description }}</div>
                <div><a :href="card.url" class="read_more">Read More <i class="fa-solid fa-chevron-right"></i></a></div>
                <div v-if="hover == index + 1" class="icona_sfondo_hover"><i :class="card.icon"></i></div>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;

.key_features {
    .title_description {
        h3 {
            font-size: 22px;
            font-weight: 600;
            margin-bottom: 20px;
            color: #161c2d;
        }

        div {
            width: 60%;
            font-size: 12px;
            @include description;

            a {
                color: $colore_primario;
            }
        }
    }

    .card_container {
        margin-top: 40px;
        display: flex;
        gap: 20px;

        .single_card {
            width: 25%;
            border: 1px solid rgb(235, 235, 235);
            border-radius: 5px;
            padding: 20px;
            position: relative;
            color: #161c2d;

            .icone {
                @include icone_quadrate;
                font-size: 20px;
                padding: 16px;
                margin-bottom: 20px
            }

            .description {
                @include description;
                font-size: 10px;
                margin: 10px 0;
            }

            .read_more {
                color: $colore_primario;
                font-weight: 600;
                font-size: 11px;
                padding: 10px 0 10px 0;

                .fa-chevron-right {
                    font-size: 10px;
                }

                &:hover {
                    background-color: #2443ac;
                    color: white;
                    padding: 10px;
                    border-radius: 5px;
                }
            }

            .icona_sfondo_hover {
                position: absolute;
                z-index: -100;
                top: 0;
                left: 0;
                width: 100%;
                height: 100%;

                i {
                    display: flex;
                    align-items: center;
                    justify-content: center;
                    width: 100%;
                    height: 100%;
                    font-size: 230px;
                    color: #f5f7fd;
                    overflow: hidden;
                }
            }

            &:hover {
                position: relative;
                bottom: 10px;
            }
        }
    }
}
</style>
