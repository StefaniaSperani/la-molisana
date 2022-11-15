<template>
  <!-- <h1>Ciao <i class="fa-solid fa-bell"></i></h1> -->
  <button class="btn btn-secondary"></button>
  <HeaderComponent />
  <main>
    <ProductList />
  </main>
  <FooterComponent />

</template>

<script>
import FooterComponent from './components/FooterComponent.vue';
import HeaderComponent from './components/HeaderComponent.vue';
import ProductList from './components/ProductList.vue';

export default {
  components: {
    HeaderComponent,
    ProductList,
    FooterComponent
  }
}
</script>

<style lang="scss">
//@use './assets/styles/general.scss' as *;

// h1 {
//   color: $colorred;
// }
</style>