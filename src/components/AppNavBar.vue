<script>
export default {
    name: "AppNavBar",
    props: {
        vociMenuHeaderOnPageHeader: Array
    },
    data() {
        return {
            itemAttivoNav: "1"
        }
    }
}
</script>

<template>
    <nav>
        <div class="logo">
            <a href="#">
                <img src="./../assets/img/logo-dark.png" alt="logo-dark">
            </a>
        </div>

        <ul>
            <li v-for="(voceMenu, index) in vociMenuHeaderOnPageHeader" :key="index">
                <a :href="voceMenu.url" :class="(itemAttivoNav == index) ? 'navActive' : ''" @click="itemAttivoNav = index">
                    {{ voceMenu.name.toUpperCase() }}
                    <span v-if="voceMenu.dropdown">
                        <i class="fa-solid fa-chevron-down"></i>
                    </span>
                </a>
            </li>
        </ul>

        <div class="icon">
            <a href="#"><i class="fa-solid fa-magnifying-glass"></i></a>
            <a href="#"><i class="fa-brands fa-github"></i></a>
            <a href="#"><i class="fa-brands fa-stack-overflow"></i></a>
            <a href="#"><i class="fa-regular fa-user"></i></a>
        </div>
    </nav>
</template>

<style scoped lang="scss">
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;

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

            &:hover {
                color: $colore_primario;
            }
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
            box-shadow: 0 1px #c6d1f2;

            &:hover {
                background-color: $colore_primario;
                color: white;
            }
        }

        .fa-user {
            font-size: 12px;
            padding: 10px;
        }
    }

}
</style>
