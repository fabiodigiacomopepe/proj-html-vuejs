<script>
export default {
    name: "AppJumbotron",
}
</script>

<template>
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
</template>

<style scoped lang="scss">
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;

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
            gap: 10px;
            font-weight: 600;
            margin: 20px 0;
            font-size: 12px;
            height: 35px;

            .blue-button {
                background-color: $colore_primario;
                border-radius: 5px;

                a {
                    display: inline-block;
                    color: white;
                    height: 100%;
                    display: flex;
                    align-items: center;
                    padding: 0 18px;
                    border-radius: 5px;

                    &:hover {
                        background-color: #2443ac;
                    }
                }
            }

            .white-button {
                background-color: white;
                border-radius: 5px;
                border: 1.5px solid $colore_primario;

                a {
                    display: inline-block;
                    color: $colore_primario;
                    height: 100%;
                    display: flex;
                    align-items: center;
                    padding: 0 12px;
                    border-radius: 5px;

                    &:hover {
                        background-color: #f6f8fa;
                        color: #1b1919;
                    }
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
</style>