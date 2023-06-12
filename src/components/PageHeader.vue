<script>
export default {
    name: "PageHeader",
    props: {
        vociMenuHeader: Array
    }
}
</script>

<template>
    <header>
        <div class="setting">
            <a href="#">
                <i class="fa-solid fa-gear"></i>
            </a>

        </div>

        <nav>
            <div class="logo">
                <a href="#">
                    <img src="./../assets/img/logo-dark.png" alt="logo-dark">
                </a>
            </div>

            <ul>
                <li v-for="voceMenu in vociMenuHeader">
                    <a :href="voceMenu.url" :class="(voceMenu.active) ? 'navActive' : ''">{{ voceMenu.name.toUpperCase()
                    }}</a>
                    <span v-if="voceMenu.dropdown" :class="(voceMenu.active) ? 'navActive' : ''"><i
                            class="fa-solid fa-chevron-down"></i></span>
                </li>
            </ul>

            <div class="icon">
                <a href="#"><i class="fa-solid fa-magnifying-glass"></i></a>
                <a href="#"><i class="fa-brands fa-github"></i></a>
                <a href="#"><i class="fa-brands fa-stack-overflow"></i></a>
                <a href="#"><i class="fa-regular fa-user"></i></a>
            </div>
        </nav>

        <section class="jumbotron">
            <div class="left-side">
                <div class="tag">Development</div>
                <h1>A Complete <br>
                    Developer Toolset
                </h1>
                <div class="description">
                    Launch your campaign and benefit from our expertise on designing and managing conversion centered
                    bootstrap4 html page.
                </div>
                <div class="button">
                    <div class="blue-button">
                        <a href="#">
                            Get Started
                        </a>
                    </div>
                    <div class="white-button">
                        <a href="#">
                            Documentation
                        </a>
                    </div>
                </div>
                <div class="description version">
                    Current Version: v.2.6.0
                </div>
            </div>

            <div class="right-side">
                <img src="./../assets/img/about.png" alt="about">
            </div>
        </section>

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
    </header>
</template>

<style scoped lang="scss">
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;

header {
    background-color: #f8f9fc;
    width: 100%;
    padding: 10px 0;
    position: relative;

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

    nav {
        width: 70%;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
        align-items: center;

        .logo {
            width: 125px;

            img {
                max-width: 100%;
            }
        }

        ul {
            display: flex;
            gap: 25px;
            font-size: 12px;
            font-weight: bold;

            a {
                color: #5c6675;
            }

            .navActive {
                color: $colore_primario;
            }

            span {
                font-size: 10px;
                margin-left: 5px;
                position: relative;
                bottom: 2px;
            }
        }

        .icon {
            display: flex;
            align-items: center;
            gap: 5px;

            .fa-magnifying-glass {
                color: #8e9bad;
                margin-right: 5px;
            }

            .fa-brands,
            .fa-regular {
                @include icone_quadrate;
            }

            .fa-user {
                font-size: 12px;
                padding: 10px;
            }

            .fa-brands:hover,
            .fa-regular:hover {
                background-color: $colore_primario;
                color: white;
            }
        }

    }

    .jumbotron {
        width: 70%;
        margin: 120px auto 60px;
        display: flex;
        gap: 40px;
        justify-content: space-between;
        align-items: center;

        .left-side {
            width: 55%;

            .tag {
                @include tag;
            }

            h1 {
                padding: 10px 0;
                font-size: 30px;
                line-height: 1.6;
                color: #161c2d;
            }

            .description {
                @include description;
                font-size: 12px;
            }

            .button {
                display: flex;
                gap: 15px;
                font-weight: 600;
                padding: 20px 0;
                font-size: 12px;

                .blue-button {
                    background-color: $colore_primario;
                    padding: 10px 15px;
                    border-radius: 5px;

                    a {
                        color: white;
                    }
                }

                .white-button {
                    background-color: white;
                    padding: 10px 15px;
                    border-radius: 5px;
                    border: 1.5px solid $colore_primario;

                    a {
                        color: $colore_primario;
                    }
                }
            }

            .version {
                font-size: 11px;
            }
        }

        .right-side {
            width: 45%;
            margin-right: 35px;

            img {
                max-width: 100%;
            }
        }
    }

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
}
</style>
