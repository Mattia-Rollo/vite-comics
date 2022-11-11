<template>
    <div class="wrapper">
        <div class="container">
            <a href="#">SIGN UP</a>

            <a class="follow" href="">FOLLOW US</a>

            <ul>
                <li v-for="(item, index) in list" :key="index">
                    <a :href="item.url"><img :src="getImagePath(`../assets/img/footer-${item.path}`)" alt=""></a>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
    nome: 'BottomFooterComponent',
    data() {
        return {
            list: [
                {
                    path: 'facebook.png',
                    url: '#'
                },
                {
                    path: 'periscope.png',
                    url: '#'
                },
                {
                    path: 'pinterest.png',
                    url: '#'
                },
                {
                    path: 'twitter.png',
                    url: '#'
                },
                {
                    path: 'youtube.png',
                    url: '#'
                }



            ]
        };
    },
    methods: {
        getImagePath: function (imgPath) {
            return new URL(imgPath, import.meta.url).href;
        }
    }
};
</script>

<style lang="scss" scoped>
@use '../assets/style/partials/mixins' as *;
@use '../assets/style/partials/variables' as *;

.wrapper {
    background-color: $almost-dark;
    color: $white;
}

.container {
    padding: 1rem 0;
    @include d-flex;
    align-items: center;
}

a {
    display: inline-block;
    text-decoration: none;
    padding: 0.7rem 1rem;
    color: $white;
    background: transparent;
    border: 1px solid $blue;
    transition: all 0.5s;

    &:hover:not(.follow, ul a) {
        background-color: $blue;
    }
}

.follow {
    font-weight: 700;
    margin-left: auto;
    border: none;
    color: $blue;

    &:hover {
        color: $blue-light;
    }
}

ul {
    list-style: none;
    @include d-flex;

    a {
        border: none;

        &:hover img {
            filter: brightness(1.8) contrast(10);
            // background-color: $blue;
        }
    }
}
</style>