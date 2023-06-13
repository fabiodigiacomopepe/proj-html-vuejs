<script>
export default {
    name: "AppQuickStart",
}
</script>

<template>
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
</template>

<style scoped lang="scss">
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;

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
</style>
