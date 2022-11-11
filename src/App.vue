<template>
  <div>
    <HeaderComponent />
  </div>
  <main>
    <ProductsList />
  </main>
  <ExtraComponent />
  <FooterComponent />
  <BottomFooterComponent />

</template>

<script>
import BottomFooterComponent from './components/BottomFooterComponent.vue';
import ExtraComponent from './components/ExtraComponent.vue';
import FooterComponent from './components/FooterComponent.vue';
import HeaderComponent from './components/HeaderComponent.vue';
import ProductsList from './components/ProductsList.vue';

export default {
  components: {
    HeaderComponent,
    ProductsList,
    FooterComponent,
    BottomFooterComponent,
    ExtraComponent
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