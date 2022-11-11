<template>
    <div>
        <ul class="container">
            <li v-for="(item, index) in lista" :key="index">
                <a href="{{item.url}}">
                    <div class="image">

                        <img :src="`./img/buy-comics-${item.imgPath}`" alt="">
                    </div>
                    <span>{{ item.text.toUpperCase() }}</span>
                </a>

            </li>
        </ul>
    </div>
</template>

<script>
import {list} from '../assets/data/data'
export default {
    name: 'ExtraComponent',
    data() {
        return {
            lista: list
        }
    },
    methods: {
        
    }
}
</script>

<style lang="scss" scoped>
@use '../assets/style/partials/mixins' as *;
@use '../assets/style/partials/variables' as *;

div {
    background: $blue;
}

ul {
    @include d-flex;
    justify-content: center;
    align-items: center;
    list-style: none;
    padding: 1rem 0;

    a {
        @include d-flex;
        justify-content: center;
        align-items: center;
        text-decoration: none;
        color: $white;

        span {
            text-align: left;
        }

        div.image {
            text-align: center;
            height: 100%;

            img {
                width: 50%;
                // margin-right: 1rem;
            }

            img[src*="svg"] {
                width: 80px;
                margin: 1rem;
            }
        }

    }
}
</style>