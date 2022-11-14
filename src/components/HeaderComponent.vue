<template>
  <header class="container">
    <div @click="!mobileView">
      <img src="/img/dc-logo.png" alt="" />
    </div>
    <Transition name="slide-fade">
      <ul v-if="!mobileView">
        <li v-for="(list, index) in lists" :key="index" :class="{ active: list.current }">
          <a :href="list.url">{{ list.text.toUpperCase() }}</a>
        </li>
      </ul>
    </Transition>
    <Transition name="slide-fade">
      <span v-if="mobileView"><i class="fa-solid fa-bars" @click=""></i></span>
    </Transition>
  </header>
</template>

<script>
export default {
  name: "HeaderComponent",
  data() {
    return {
      mobileView: false,
      check: true,
      lists: [
        {
          text: "characters",
          url: "#",
          current: false,
        },
        {
          text: "comics",
          url: "#",
          current: false,
        },
        {
          text: "movies",
          url: "#",
          current: false,
        },
        {
          text: "tv",
          url: "#",
          current: false,
        },
        {
          text: "games",
          url: "#",
          current: true,
        },
        {
          text: "collectibles",
          url: "#",
          current: false,
        },
        {
          text: "videos",
          url: "#",
          current: false,
        },
        {
          text: "fans",
          url: "#",
          current: false,
        },
        {
          text: "news",
          url: "#",
          current: false,
        },
        {
          text: "shop",
          url: "#",
          current: false,
        },
      ],
    };
  },
  methods: {
    handleView() {
      this.mobileView = window.innerWidth <= 900;
    },
  },
  created() {
    window.addEventListener("resize", this.handleView);
  },
};
</script>

<style lang="scss" scoped>
@use '../assets/style/partials/mixins' as *;
@use '../assets/style/partials/variables' as *;

header {
  @include d-flex;
  justify-content: space-between;
  align-items: center;
  height: 80px;
  position: relative;

  // align-items: center;
  div {
    padding: 0.3rem;
    // width: 50px;
    height: 100%;

    img {
      max-height: 100%;
      display: inline-block;
    }
  }
}

ul {
  list-style: none;
  height: 100%;
  // background-color: aqua;
  @include d-flex;
  @media screen and (max-width: 950px) {
    flex-direction: column;
    position: absolute;
    width: 100%;
    background-color: white;
    top: 80px;
    height: auto;
    z-index: 10;
  }

  li {
    @include d-flex;
    padding: 0 1rem;
  }

  li a {
    @include d-flex;
    font-weight: 700;
    align-items: center;
    border-bottom: 5px solid transparent;
    text-decoration: none;
    color: $black-bg-main;
    // padding: 0 1rem;
    transition: all 0.4s;
    @media screen and (max-width: 950px) {
      padding: 0.8rem 0;
      width: 100%;
    }

    &.active,
    &:hover {
      color: $blue;
      border-bottom-color: $blue;
    }
  }
}
span {
  display: inline-block;
  padding: 1rem;
  font-size: 1.5rem;
}
// span:after {
//   content: "\f0c9";
//   font-weight: 600;
//   font-size: 1rem;
//   font-family: "Font Awesome 6 Free";
// }

.slide-fade-enter-active {
  transition: all 0.2s ease-out;
}

.slide-fade-leave-active {
  transition: all 0.2s cubic-bezier(1, 0.5, 0.8, 1);
}

.slide-fade-enter-from,
.slide-fade-leave-to {
  transform: translateY(-20px);
  opacity: 0;
}
</style>
