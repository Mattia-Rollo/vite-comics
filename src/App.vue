<template>
  <div>
    <HeaderComponent />
  </div>
  <div>
    <ProductsList />
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import ProductsList from './components/ProductsList.vue';

  export default {
    components: {
    HeaderComponent,
    ProductsList
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