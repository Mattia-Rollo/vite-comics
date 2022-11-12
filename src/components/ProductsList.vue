<template>
  <div class="wrapper">
    <div class="container">
      <div class="info">CURRENT SERIES</div>
      <div class="container">
        <div class="row">
          <Card v-for="(comic, index) in comics" :src="comic.thumb" :key="index" :title="comic.series" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Card from "./Card.vue";
import { comics } from "../assets/data/data";
export default {
  name: "ProductsList",
  components: {
    Card,
  },
  data() {
    return {
      comics: comics,
    };
  },
};
</script>

<style lang="scss">
@use '../assets/style/partials/mixins' as *;
@use '../assets/style/partials/variables' as *;

div.wrapper {
  background-color: $black-bg-main;
  color: $white;
  padding: 1rem 0;

  div.container {
    position: relative;

    div.info {
      position: absolute;
      top: -2.5rem;
      padding: 1rem;
      background-color: $blue;
      font-weight: 700;
    }

    div.row {
      @include d-flex;
      flex-wrap: wrap;
      padding: 1.5rem 0;
      gap: 1rem 0;

      div.card {
        width: calc(100% / 6);
        padding: 0 1rem;

        a {
          text-decoration: none;
          color: $white;
        }

        img {
          height: 170px;
          width: 100%;
          object-fit: cover;
          object-position: top;
        }

        div {
          text-align: center;
        }

        @media screen and (max-width: 850px) {
          width: calc(100% / 4);
        }

        @media screen and (max-width: 540px) {
          width: calc(100% / 2);
        }
      }
    }
  }
}
</style>
