<script>
export default {
    name: "AppGetStarted",
}
</script>

<template>
    <section class="get_started">
        <div class="title_description">
            <h3>Want to be among the first to find out?</h3>
            <div class="description">Start working with <a href="#">Landrick</a> that can provide everything you need to
                generate awareness, drive traffic, connect.
            </div>
        </div>
        <div>
            <form action="#">
                <input type="email" name="email" id="email" placeholder="Email Address">
                <button type="button">Get Started</button>
            </form>
        </div>
    </section>
</template>

<style scoped lang="scss">
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;

.get_started {
    text-align: center;

    .title_description {
        margin-top: 70px;

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

    form {
        width: 55%;
        margin: 0 auto;
        position: relative;

        input {
            width: 100%;
            padding: 15px 120px 15px 15px;
            margin-bottom: 90px;
            border: 1px solid #c0c5cb;
            border-radius: 30px;

        }

        button {
            position: absolute;
            top: 6px;
            right: 5px;
            width: 100px;
            border-radius: 20px;
            padding: 10px;
            background-color: $colore_primario;
            color: white;
            font-weight: bold;
            border: none;

            &:hover {
                cursor: pointer;
                background-color: #2443ac;
            }
        }
    }
}
</style>
