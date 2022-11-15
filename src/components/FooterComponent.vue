<template>
    <footer>
        <div class="cols container">
            <a href="#" class="logo">
                <img src="../assets/img/la-molisana-logo.png" alt="La Molisana">
            </a>
            <FooterMenu v-for="(menu, index) in navBars" :key="index" :item="menu" />

        </div>

    </footer>
</template>

<script>
import { menu } from '../data/products';
import FooterMenu from './FooterMenu.vue';
export default {
    name: 'FooterComponent',
    components: {
        FooterMenu
    },
    data() {
        return {
            navBars: menu
        }
    }
}
</script>

<style lang="scss">
@use '../assets/styles/partials/mixins' as *;
@use '../assets/styles/partials/variables' as *;

footer {
    padding-top: 3rem;
    background-image: url('../assets/img/footer-montagne-bottom.jpg');
    background-repeat: no-repeat;
    background-position: bottom;
    padding-bottom: 1rem;

    .cols {
        display: flex;


        .logo,
        .footer-links {
            flex-basis: calc(100% / 3);
            padding: 0 1rem;
        }

        h4 {
            text-transform: uppercase;
            font-size: 1.25em;
            font-weight: 600;
            margin-bottom: 1rem;
            color: $bluetext;
        }

        ul {
            list-style: none;

            li a {
                display: inline-block;
                margin-bottom: 0.25rem;
                text-decoration: none;
                font-size: 0.875em;


                &:hover {
                    color: $bluetext;
                }
            }
        }
    }
}
</style>