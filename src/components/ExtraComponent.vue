<template>
  <div>
    <ul class="container">
      <li v-for="(item, index) in lista" :key="index">
        <a href="{{item.url}}">
          <div class="image">
            <img :src="`./img/buy-comics-${item.imgPath}`" alt="" />
          </div>
          <span>{{ item.text.toUpperCase() }}</span>
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
import { list } from "../assets/data/data";
export default {
  name: "ExtraComponent",
  data() {
    return {
      lista: list,
    };
  },
  methods: {},
};
</script>

<style lang="scss" scoped>
@use '../assets/style/partials/mixins' as *;
@use '../assets/style/partials/variables' as *;

div {
  background: $blue;
}

ul {
  @include d-flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  list-style: none;
  padding: 1rem 1rem;

  a {
    @include d-flex;
    justify-content: center;
    align-items: center;
    text-decoration: none;
    color: $white;

    span {
      text-align: right;
    }

    div.image {
      text-align: center;
      // height: 50%;

      img {
        max-width: 100%;
        height: 60px;
        width: 100px;
        margin-right: 1rem;
      }

      img[src*="svg"] {
        height: 40px;
        margin-right: 1rem;
      }
    }
  }
}
</style>
