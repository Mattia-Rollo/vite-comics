<template>
  <div class="wrapper">
    <div class="container">
      <!-- stampo 3 ul sapendo già la lunghezza dell'array me ne stamperà 3 ma  -->
      <ul v-for="(item, index) in footerMenu" :key="index">
        <!-- se il primo item è un array stampami tante ul quanto è lungo l'array -->
        <!-- per ogni ul mi stampi ogni singolo oggetto  uno sotto l'altro -->
        <ul v-if="Array.isArray(item)" v-for="(i, index) in item" :key="index">
          <h4>{{ i.title }}</h4>
          <li v-for="(a, index) in i.links" :key="index">
            <a href="#">{{ a.linkText }}</a>
          </li>
        </ul>
        <!-- altrimenti stampami le ul normalemte-->
        <h4 v-else>{{ item.title }}</h4>
        <li v-for="(link, index) in item.links" :key="index">
          <a :href="link.url">{{ link.linkText }}</a>
        </li>
      </ul>
      <div class="logo"></div>
    </div>
  </div>
</template>

<script>
import { footerMenu } from "../assets/data/data";
export default {
  name: "FooterComponent",
  data() {
    return {
      footerMenu,
    };
  },
};
</script>

<style lang="scss" scoped>
@use "../assets/style/partials/mixins" as *;
@use "../assets/style/partials/variables" as *;

.wrapper {
  background-color: $almost-dark;
  background-image: url("/img/footer-bg.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  overflow: hidden;
}

div.container {
  position: relative;
  @include d-flex;
  padding: 1rem 1rem;

  // background: transparent;s
  ul {
    margin: 0;
    list-style: none;
    padding: 0 2rem 1rem 0;
    color: $grey;

    h4 {
      text-transform: uppercase;
      color: $white;
      font-size: 1.2rem;
      padding: 1rem 0;
    }

    // li:first-child a {
    //   display: inline-block;
    //   text-transform: uppercase;
    //   color: $white;
    //   font-size: 1.2rem;
    //   padding: 1rem 0;
    // }

    ul {
      padding: 0;
    }

    li a {
      text-decoration: none;
      padding: 5px 0;
      color: $grey;
      display: inline-block;
      padding: 0.2rem 0;
      &:hover {
        color: $white;
      }
    }
  }
}

.logo {
  background-image: url("/img/dc-logo-bg.png");
  background-repeat: no-repeat;
  background-position: center;
  background-size: auto;
  // background-color: transparent;
  position: absolute;
  right: 0;
  top: 50%;
  transform: translateY(-50%);

  width: 560px;
  height: 130%;
}
</style>
