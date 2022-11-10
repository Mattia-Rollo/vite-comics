<template>
  <div>
    <HeaderComponent />
  </div>
  <main>
    <ProductsList />
  </main>
  <footer>
    <FooterComponent />
  </footer>
</template>

<script>
import FooterComponent from './components/FooterComponent.vue';
import HeaderComponent from './components/HeaderComponent.vue';
import ProductsList from './components/ProductsList.vue';

  export default {
    components: {
    HeaderComponent,
    ProductsList,
    FooterComponent
},
      data() {
        return {
          
        }
      },
}
</script>

<style lang="scss" scoped>
@use './assets/style/partials/mixins' as *;
@use './assets/style/partials/variables' as *;



</style>