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
    </header>
</template>

<style scoped lang="scss">
@use '../styles/partials/variables.scss' as *;
@use '../styles/partials/mixins.scss' as *;

header {
    background-color: #f8f9fc;
    width: 100%;
    padding: 10px 0;

    nav {
        width: 70%;
        margin: 0 auto;
        display: flex;
        justify-content: space-between;
        align-items: center;

        .logo {
            width: 130px;

            img {
                max-width: 100%;
            }
        }

        ul {
            display: flex;
            gap: 25px;
            font-weight: 500;

            .navActive {
                color: #355ad5;
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
            gap: 8px;

            .fa-magnifying-glass {
                color: #8e9bad;
                margin-right: 5px;
            }

            .fa-brands,
            .fa-regular {
                color: #3a5ed5;
                background-color: #e4e9f8;
                padding: 10px;
                border-radius: 5px;
                border: 1px solid #d8e0f6;
            }

            .fa-user {
                font-size: 12px;
                padding: 12px;
            }

            .fa-brands:hover,
            .fa-regular:hover {
                background-color: #2f55d4;
                color: white;
            }
        }

    }
}
</style>
