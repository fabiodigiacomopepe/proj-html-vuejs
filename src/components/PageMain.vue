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

        <section class="build_tools">
            <div class="left-side">
                <h3>Build tools and<br>extensive documention</h3>
                <div class="description">You can combine all the Landrick templates into a single one, you can take a
                    component from the Application theme and use it in the Website.</div>
                <ul>
                    <li><i class="fa-regular fa-circle-check"></i> Digital Marketing Solutions for Tomorrow</li>
                    <li><i class="fa-regular fa-circle-check"></i> Our Talented & Experienced Marketing Agency</li>
                    <li><i class="fa-regular fa-circle-check"></i> Create you own skin to match your brand</li>
                </ul>
                <div><a href="#" class="read_more">Read More <i class="fa-solid fa-arrow-right"></i></a></div>
            </div>

            <div class="right-side">
                <img src="./../assets/img/1.png" alt="grafico">
            </div>
        </section>

        <section class="price">
            <div class="title_description">
                <h3>Our rates for developer from landrick team</h3>
                <div class="description">Start working with <span>Landrick</span> that can provide everything you need to
                    generate awareness, drive traffic, connect.
                </div>
            </div>

            <div class="card_container">
                <div class="single_card">
                    <h5>Basic</h5>
                    <h2>$9.00</h2>
                    <div class="duration">Per Month</div>
                    <div class="description_price">All the basics for businesses that are just getting started.</div>
                    <ul>
                        <li><i class="fa-regular fa-circle-check"></i> Full Access</li>
                        <li><i class="fa-regular fa-circle-check"></i> Enchanced Security</li>
                        <li><i class="fa-regular fa-circle-check"></i> Source Files</li>
                        <li><i class="fa-regular fa-circle-check"></i> 1 Domain Free</li>
                        <li><i class="fa-regular fa-circle-check"></i> Enchanced Security</li>
                    </ul>
                    <div><a href="#">Buy Now</a></div>
                    <div>*No credit card required</div>
                </div>

                <div class="single_card">
                    <h5>Business</h5>
                    <h2>$39.00</h2>
                    <div class="duration">Per Month</div>
                    <div class="description_price">Better for growing businesses that want more customers.</div>
                    <ul>
                        <li><i class="fa-regular fa-circle-check"></i> Full Access</li>
                        <li><i class="fa-regular fa-circle-check"></i> Enchanced Security</li>
                        <li><i class="fa-regular fa-circle-check"></i> Source Files</li>
                        <li><i class="fa-regular fa-circle-check"></i> 1 Domain Free</li>
                        <li><i class="fa-regular fa-circle-check"></i> Enchanced Security</li>
                    </ul>
                    <div><a href="#">Buy Now</a></div>
                    <div>*No credit card required</div>
                    <div class="best_price">
                        <img src="./../assets/img/best_price.png" alt="best">
                    </div>
                </div>

                <div class="single_card">
                    <h5>Enterprise</h5>
                    <h2>$79.00</h2>
                    <div class="duration">Per Month</div>
                    <div class="description_price">Advanced features for pros who need more customization.</div>
                    <ul>
                        <li><i class="fa-regular fa-circle-check"></i> Full Access</li>
                        <li><i class="fa-regular fa-circle-check"></i> Enchanced Security</li>
                        <li><i class="fa-regular fa-circle-check"></i> Source Files</li>
                        <li><i class="fa-regular fa-circle-check"></i> 1 Domain Free</li>
                        <li><i class="fa-regular fa-circle-check"></i> Enchanced Security</li>
                    </ul>
                    <div><a href="#">Buy Now</a></div>
                    <div>*No credit card required</div>
                </div>
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
    margin-top: 70px;

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
        width: 65%;
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
                color: #161c2d;
            }

            div {
                @include description;
                font-size: 11px;
                width: 90%;
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
                font-size: 11px;

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
            font-size: 11px;
            margin-top: 20px;

            .simbolo {
                color: #2ebf86;
                font-size: 14px;
                margin-right: 5px;
            }
        }
    }

    .build_tools {
        margin-top: 110px;
        display: flex;
        justify-content: space-around;

        .left-side {
            width: 55%;

            h3 {
                font-size: 22px;
                line-height: 1.6;
                margin-bottom: 20px;
                color: #161c2d;
            }

            .description {
                width: 95%;
                font-size: 11px;
                line-height: 1.6;
                font-weight: 600;
                color: #7d8b9f;
                margin-bottom: 15px;
            }

            ul {
                color: #7d8b9f;
                font-weight: 600;
                font-size: 11px;
                line-height: 1.6;
                margin-bottom: 20px;

                i {
                    font-size: 14px;
                    margin-right: 5px;
                    color: $colore_primario;
                }
            }

            .read_more {
                background-color: $colore_primario;
                color: white;
                font-weight: 600;
                font-size: 12px;
                padding: 10px 15px;
                border-radius: 5px;

                i {
                    margin-left: 5px
                }
            }

            .read_more:hover {
                background-color: #2443ac;
            }
        }

        .right-side {
            width: 40%;

            img {
                max-width: 100%;
                margin-left: 10px;
                position: relative;
                bottom: 20px;
            }
        }
    }

    .price {
        text-align: center;

        .title_description {
            margin-top: 35px;

            h3 {
                color: #161c2d;
                font-size: 21px;
                margin-bottom: 30px;
            }

            .description {
                font-size: 11px;
                line-height: 1.6;
                width: 55%;
                margin: 0 auto 50px;
                font-weight: bold;
                color: #7d8b9f;

                span {
                    color: $colore_primario;
                }
            }
        }

        .card_container {
            display: flex;
            gap: 20px;
            text-align: left;
            margin-bottom: 50px;

            .single_card {
                width: calc(100% / 3);
                border: 1px solid #dfe0e2;
                padding: 20px;
                border-radius: 8px;
                color: #7d8b9f;
                font-weight: 600;
                font-size: 11px;
                position: relative;
                box-shadow: 0 2px rgb(170, 170, 170);

                h5 {
                    @include tag;
                    padding: 10px 20px;
                    font-size: 11px;
                    border-radius: 20px;
                    margin-bottom: 10px;
                }

                h2 {
                    font-size: 26px;
                    margin-bottom: 8px;
                    color: #161c2d;
                }

                .duration {
                    margin-bottom: 10px;
                }

                .description_price {
                    border-bottom: 1px solid #dfe0e2;
                    padding-bottom: 10px;
                    margin-bottom: 10px;
                }

                ul {
                    font-size: 12px;
                    line-height: 1.6;
                    margin-bottom: 20px;

                    .fa-circle-check {
                        color: $colore_primario;
                        margin-right: 5px;
                    }
                }

                a {
                    display: inline-block;
                    text-align: center;
                    width: 100%;
                    background-color: $colore_primario;
                    color: white;
                    font-weight: 600;
                    font-size: 12px;
                    padding: 10px 0;
                    border-radius: 5px;
                    margin-bottom: 10px;
                }

                a:hover {
                    background-color: #2443ac;
                }

                .best_price {
                    position: absolute;
                    top: -6px;
                    right: -6px;
                    width: 60px;

                    img {
                        max-width: 100%;
                    }
                }
            }

            .single_card:hover {
                scale: 1.05;
                box-shadow: 0 2px #2443ac;
            }
        }
    }
}
</style>
