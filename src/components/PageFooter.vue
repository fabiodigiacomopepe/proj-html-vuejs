<script>
export default {
    name: "PageFooter",
    props: {
        vociCompany: Array,
        vociUsefullLinks: Array
    },
    methods: {
        goToTheTop() {
            scroll(0, 0)
        }
    }
}
</script>

<template>
    <footer>
        <div class="up_section">
            <section>
                <div class="first-col">
                    <img src="./../assets/img/logo-light.png" alt="logo-light">
                    <div class="description">Start working with Landrick that can provide everything you need to
                        generate awareness, drive traffic, connect.
                    </div>
                    <a href="#"><i class="fa-brands fa-facebook-f"></i></a>
                    <a href="#"><i class="fa-brands fa-instagram"></i></a>
                    <a href="#"><i class="fa-brands fa-twitter"></i></a>
                    <a href="#"><i class="fa-brands fa-linkedin-in"></i></a>
                </div>

                <div class="second-col">
                    <h4>Company</h4>
                    <ul>
                        <li v-for="(voce, index) in vociCompany" :key="index">
                            <a :href=voce.url>
                                <i class="fa-solid fa-chevron-right"></i>{{ voce.name }}
                            </a>
                        </li>
                    </ul>
                </div>

                <div class="third-col">
                    <h4>Usefull Links</h4>
                    <ul>
                        <li v-for="(voce1, index1) in vociUsefullLinks" :key="index1">
                            <a :href=voce1.url>
                                <i class="fa-solid fa-chevron-right"></i>{{ voce1.name }}
                            </a>
                        </li>
                    </ul>
                </div>

                <div class="fourth-col">
                    <h4>Newsletter</h4>
                    <div class="description">Sign up and receive the latest tips via email.</div>
                    <div class="write_email">Write your email <span>*</span></div>
                    <div class="input_email">
                        <i class="fa-regular fa-envelope"></i> Your email:
                        <form action="#">
                            <input type="email">
                        </form>
                    </div>
                    <div class="subscribe">
                        <form action="#">
                            <button type="button">Subscribe</button>
                        </form>
                    </div>
                </div>
            </section>
        </div>

        <div class="down_section">
            <div class="top" @click="goToTheTop()"><i class="fa-solid fa-arrow-up"></i></div>
            <section>
                <div>
                    <i class="fa-regular fa-copyright"></i> 2020 Landrick. Dedsign with <span> &hearts;</span> by
                    Shreethemes.
                </div>

                <div>
                    <img src="./../assets/img/american-ex.png" alt="american-ex">
                    <img src="./../assets/img/discover.png" alt="discover">
                    <img src="./../assets/img/master-card.png" alt="master-card">
                    <img src="./../assets/img/paypal.png" alt="paypal">
                    <img src="./../assets/img/visa.png" alt="visa">
                </div>
            </section>
        </div>
    </footer>
</template>

<style scoped lang="scss">
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;

footer {
    background-color: #202942;
    color: #a0a8b1;
    font-weight: 600;

    .up_section {
        border-bottom: 1px solid #313c5e;

        section {
            width: 70%;
            margin: 0 auto;
            padding: 60px 0 50px;
            display: flex;

            .first-col {
                width: 30%;
                margin-right: 30px;

                img {
                    width: 125px;
                    margin-bottom: 20px;
                }

                div {
                    margin-bottom: 20px;
                    font-size: 10px;
                    line-height: 1.6;
                }

                a {
                    color: #a0a8b1;
                }

                i {
                    border: 1px solid #a0a8b1;
                    margin-right: 5px;
                    border-radius: 5px;
                    width: 30px;
                    height: 30px;
                    text-align: center;
                    line-height: 30px;
                }

                i:hover {
                    background-color: #030334;
                }
            }

            .second-col,
            .third-col {
                width: 18%;
            }

            .second-col,
            .third-col,
            .fourth-col {

                h4 {
                    color: #f6f7f7;
                    margin-bottom: 20px;
                }

                li {
                    font-size: 11px;
                    line-height: 2.4;

                    a {
                        color: #a0a8b1;
                    }

                    i {
                        margin-right: 10px;
                    }
                }
            }

            .fourth-col {
                margin-left: 60px;
                width: 23%;

                div {
                    font-size: 11px;
                    line-height: 1.6;
                }

                .description {
                    margin-bottom: 15px;
                }

                .write_email {
                    span {
                        color: #e03e51;
                    }
                }

                .input_email {
                    font-size: 10px;
                    display: flex;
                    padding: 10px 15px;
                    align-items: center;
                    margin-top: 10px;
                    width: 100%;
                    background-color: #27314f;
                    border-radius: 5px;

                    i {
                        margin-right: 10px;
                        font-size: 14px;
                    }

                    input {
                        background-color: #27314f;
                        border: none;
                        width: 80px;
                        margin-left: 5px;
                        overflow-x: auto;
                        color: white;

                    }
                }

                .subscribe {
                    margin-top: 20px;
                    border-radius: 5px;
                    box-shadow: 1px 1px #2c4dbd;

                    button {
                        width: 100%;
                        height: 30px;
                        background-color: #222e51;
                        color: #2b4cb9;
                        font-weight: 600;
                        border: none;
                        cursor: pointer;
                    }

                    button:hover {
                        background-color: #2b3962;
                        color: #d3cccc;
                    }
                }
            }
        }
    }

    .down_section {
        width: 70%;
        font-weight: 500;
        font-size: 11px;
        margin: 0 auto;
        height: 60px;
        position: relative;

        .top {
            position: absolute;
            bottom: 15px;
            right: -150px;
            background-color: #2b48aa;
            width: 30px;
            text-align: center;
            line-height: 30px;
            height: 30px;
            border-radius: 5px;
        }

        .top:hover {
            background-color: #8895bd;
            color: black;
        }

        section {
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 100%;

            span {
                color: #e43f52;
                font-size: 15px;
            }

            img {
                width: 30px;
                padding: 0 2px;
            }
        }
    }
}
</style>
