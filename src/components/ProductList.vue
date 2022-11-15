<template>
    <section class="products">
        <div class="container">
            <h1>Prodotti</h1>
            <div class="row">
                <!-- <ProductComponent v-for="(item, index) in pastas" :key="index" :img="item.src" :title="item.titolo" /> -->
                <ProductComponent v-for="(item, index) in pastas" :key="index" :obj="item" />
            </div>
        </div>
    </section>
</template>

<script>
import { products } from '../data/products.js';
import ProductComponent from './ProductComponent.vue';

export default {
    name: 'ProductList',
    components: {
        ProductComponent
    },
    data() {
        return {
            pastas: products,
        }
    },
    mounted() {
        console.log(this.pastas);
    }
}
</script>

<style lang="scss">
@use '../assets/styles/partials/mixins' as *;
@use '../assets/styles/partials/variables' as *;


.products {
    padding: 2rem 1rem;
    text-align: center;
    background-image: url("../assets/img/fondo-pag-speciali.jpg");


    h1 {
        color: $bluetext;
        margin-bottom: 20px;
    }

    .row {
        @include dflex;

        .col {
            flex-basis: calc(100% / 4);
            padding: 2rem;

            h4 {
                background-color: #fff;
                color: $bluetext;
            }
        }


    }

}
</style>