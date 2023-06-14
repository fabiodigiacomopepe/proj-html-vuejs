<script>
export default {
    name: "AppBuildTools",
}
</script>

<template>
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
</template>

<style scoped lang="scss">
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;

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

            &:hover {
                background-color: #2443ac;
            }
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
</style>
