<script>
export default {
    name: "PageMain",
    data() {
        return {
            hover: ""
        }
    }
}
</script>

<template>
    <main>
        <section class="key_features">
            <div class="title_description">
                <h3>Key Features</h3>
                <div>Start working with <a href="#">Landrick</a> that can provide everything you need to generate awareness,
                    drive
                    traffic, connect.</div>
            </div>

            <div class="card_container">
                <div class="single_card" @mouseover="hover = 1" @mouseleave="hover = 0">
                    <a href="#"><i class="fa-solid fa-layer-group icone"></i></a>
                    <h5>Modular</h5>
                    <div class="description">Composed in a pseudo-Latin language which more or less corresponds.</div>
                    <div><a href="#" class="read_more">Read More <i class="fa-solid fa-chevron-right"></i></a></div>
                    <div v-if="hover == 1" class="icona_sfondo_hover"><i class="fa-solid fa-layer-group"></i></div>
                </div>

                <div class="single_card" @mouseover="hover = 2" @mouseleave="hover = 0">
                    <a href="#"><i class="fa-solid fa-display icone"></i></a>
                    <h5>Responsive</h5>
                    <div class="description">Composed in a pseudo-Latin language which more or less corresponds.</div>
                    <div><a href="#" class="read_more">Read More <i class="fa-solid fa-chevron-right"></i></a></div>
                    <div v-if="hover == 2" class="icona_sfondo_hover"><i class="fa-solid fa-display"></i></div>
                </div>

                <div class="single_card" @mouseover="hover = 3" @mouseleave="hover = 0">
                    <a href="#"><i class="fa-solid fa-location-crosshairs icone"></i></a>
                    <h5>Customizable</h5>
                    <div class="description">Composed in a pseudo-Latin language which more or less corresponds.</div>
                    <div><a href="#" class="read_more">Read More <i class="fa-solid fa-chevron-right"></i></a></div>
                    <div v-if="hover == 3" class="icona_sfondo_hover"><i class="fa-solid fa-location-crosshairs"></i></div>
                </div>

                <div class="single_card" @mouseover="hover = 4" @mouseleave="hover = 0">
                    <a href="#"><i class="fa-solid fa-maximize icone"></i></a>
                    <h5>Scalable</h5>
                    <div class="description">Composed in a pseudo-Latin language which more or less corresponds.</div>
                    <div><a href="#" class="read_more">Read More <i class="fa-solid fa-chevron-right"></i></a></div>
                    <div v-if="hover == 4" class="icona_sfondo_hover"><i class="fa-solid fa-maximize"></i></div>
                </div>
            </div>
        </section>

        <section class="quickstart">
            <div class="description">
                <h5>Quickstart</h5>
                <h3>Awesome isn't it? Let's dive in!</h3>
                <div>Start working with <a href="#">Landrick</a> that can provide everything you need to generate awareness,
                    drive traffic, connect</div>
            </div>

            <div class="install_method">
                <ul>
                    <li class="active">npm</li>
                    <li>nuget</li>
                    <li>spm</li>
                    <li>github</li>
                </ul>
                <div class="code">
                    <span><span class="simbolo">$</span> npm install </span>
                    <span><span class="simbolo">-g</span> claps.js</span>
                </div>
            </div>

            <div class="check">
                <div><span class="simbolo"><i class="fa-regular fa-circle-check"></i></span> Organize your data</div>
                <div><span class="simbolo"><i class="fa-regular fa-circle-check"></i></span> Work with any team</div>
            </div>
        </section>
    </main>
</template>

<style scoped lang="scss">
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;

main {
    width: 70%;
    margin: 0 auto;
    min-height: 800px;
    margin-top: 70px;

    .key_features {
        .title_description {
            h3 {
                font-size: 22px;
                font-weight: 600;
                margin-bottom: 20px;
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
                }

                .read_more:hover {
                    background-color: #2443ac;
                    color: white;
                    padding: 10px;
                    border-radius: 5px;
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
            }

            .single_card:hover {
                position: relative;
                bottom: 10px;
            }
        }
    }

    .quickstart {
        width: 70%;
        margin: 80px auto 0;

        .description {
            text-align: center;

            h5 {
                color: $colore_primario;
                margin-bottom: 20px;
            }

            h3 {
                font-size: 22px;
                margin-bottom: 20px;
            }

            div {
                @include description;
                font-size: 11px;
                width: 75%;
                margin: 0 auto;

                a {
                    color: $colore_primario;
                }
            }
        }

        .install_method {
            margin-top: 40px;
            background-color: #3c4858;
            width: 100%;
            border-radius: 8px;
            padding: 20px;

            ul {
                display: flex;
                color: white;
                border: 1px solid #4e5968;
                border-radius: 5px;
                background-color: #4e5968;
                cursor: pointer;

                li {
                    width: 25%;
                    text-align: center;
                    border: 1px solid #4e5968;
                    padding: 5px 0;
                    border-radius: 5px;
                }

                .active {
                    background-color: #3c4858;
                }
            }

            .code {
                font-weight: bold;
                color: #7d8b9f;
                margin-top: 10px;
                font-size: 12px;

                .simbolo {
                    color: #2ebf86;
                }
            }
        }

        .check {
            display: flex;
            gap: 40px;
            color: #7d8b9f;
            font-weight: 600;
            font-size: 12px;
            margin-top: 20px;

            .simbolo {
                color: #2ebf86;
                font-size: 14px;
                margin-right: 5px;
            }
        }
    }
}
</style>
