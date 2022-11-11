<template>
    <header class="container">
        <div>
            <img src="../../public/img/dc-logo.png" alt="">
        </div>
        <ul>
            <li v-for="(list, index) in lists" :key="index" :class="{ 'active': list.current }">
                <a :href="list.url">{{ list.text.toUpperCase() }}</a>
            </li>
        </ul>
    </header>
</template>

<script>
export default {
    name: 'HeaderComponent',
    data() {
        return {
            lists: [
                {
                    text: 'characters',
                    url: '#',
                    current: false
                },
                {
                    text: 'comics',
                    url: '#',
                    current: false
                },
                {
                    text: 'movies',
                    url: '#',
                    current: false
                },
                {
                    text: 'tv',
                    url: '#',
                    current: false
                },
                {
                    text: 'games',
                    url: '#',
                    current: false
                },
                {
                    text: 'collectibles',
                    url: '#',
                    current: false
                },
                {
                    text: 'videos',
                    url: '#',
                    current: false
                },
                {
                    text: 'fans',
                    url: '#',
                    current: false
                },
                {
                    text: 'news',
                    url: '#',
                    current: false
                },
                {
                    text: 'shop',
                    url: '#',
                    current: false
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
@use '../assets/style/partials/mixins' as *;
@use '../assets/style/partials/variables' as *;

header {
    @include d-flex;
    justify-content: space-between;
    // align-items: center;

}

ul {
    list-style: none;
    // height: 100%;
    // background-color: aqua;
    @include d-flex;

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
        transition: all .4s;

        &.active,
        &:hover {
            color: $blue;
            border-bottom-color: $blue;
        }
    }
}
</style>