<template>
    <header>
        <!-- <h1>Header</h1> -->
        <a href="#">
            <img src="../assets/img/la-molisana-logo.png" alt="La Molisana">
            <!-- <img :src="getImageURL(image)" alt="La Molisana"> -->
        </a>
        <nav>
            <!-- <ul class="d-flex justify-content-center align-items-center"> -->
            <ul>
                <li v-for="(link, index) in navbar" :key="index">
                    <a :href="link.url" :class="{ 'active': link.current }">{{ link.text }}</a>
                </li>
            </ul>
        </nav>
    </header>
</template>

<script>
import { links } from '../data/products.js'
export default {
    name: 'HeaderComponent',
    data() {
        return {
            image: '../assets/img/la-molisana-logo.png', //non funziona se non con metodo
            navbar: links
        }
    },
    methods: {
        //     getImageURL: function (imgPath) {
        //         return new URL(imgPath, import.meta.url).href;
        //     }
    }
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/partials/mixins' as *;
@use '../assets/styles/partials/variables' as *;

header {
    text-align: center;

    ul {
        list-style: none;
        margin: 2.5rem 1rem 4rem;
        @include dflex;

        li a {
            display: inline-block;
            padding: 1rem;
            text-decoration: none;
            font-weight: 600;


            &.active,
            &:hover {
                background: $lightblue;
            }
        }
    }

}
</style>