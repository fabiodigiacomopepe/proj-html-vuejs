<script>
export default {
    name: "AppPrice",
    data() {
        return {
            hover: "",
            cards: [
                {
                    tag: "Basic",
                    price: "$9.00",
                    description: "All the basics for businesses that are just getting started.",
                    bestprice: false
                },
                {
                    tag: "Business",
                    price: "$39.00",
                    description: "Better for growing businesses that want more customers.",
                    bestprice: true
                },
                {
                    tag: "Enterprise",
                    price: "$79.00",
                    description: "Advanced features for pros who need more customization.",
                    bestprice: false

                },
            ]
        }
    }
}
</script>

<template>
    <section class="price">
        <div class="title_description">
            <h3>Our rates for developer from landrick team</h3>
            <div class="description">Start working with <a href="#">Landrick</a> that can provide everything you need to
                generate awareness, drive traffic, connect.
            </div>
        </div>

        <div class="card_container">
            <div class="single_card" v-for="(card, index) in cards" :key="index">
                <h5>{{ card.tag }}</h5>
                <h2>{{ card.price }}</h2>
                <div class="duration">Per Month</div>
                <div class="description_price">{{ card.description }}</div>
                <ul>
                    <li><i class="fa-regular fa-circle-check"></i> Full Access</li>
                    <li><i class="fa-regular fa-circle-check"></i> Enchanced Security</li>
                    <li><i class="fa-regular fa-circle-check"></i> Source Files</li>
                    <li><i class="fa-regular fa-circle-check"></i> 1 Domain Free</li>
                    <li><i class="fa-regular fa-circle-check"></i> Enchanced Security</li>
                </ul>
                <div><a href="#">Buy Now</a></div>
                <div>*No credit card required</div>
                <div class="best_price" v-if="card.bestprice">
                    <img src="./../assets/img/best_price.png" alt="best">
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;

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

            a {
                color: $colore_primario;
            }
        }
    }

    .card_container {
        display: flex;
        gap: 20px;
        text-align: left;

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
</style>
