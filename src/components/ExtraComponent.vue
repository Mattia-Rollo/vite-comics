<template>
    <div>
        <ul class="container">
            <li v-for="(item,index) in list" :key="index">
                <a href="{{item.url}}">
                <div class="image">
                    
                        <img :src="getImagePath(`../assets/img/buy-comics-${item.imgPath}`)" alt="">
                </div>
                    <span>{{item.text.toUpperCase()}}</span>
                </a>
                
            </li>
        </ul>
    </div>
</template>

<script>
    export default {
        name: 'ExtraComponent',
        data() {
            return{
        list: [
            {
                imgPath: 'digital-comics.png',
                url: '#',
                text: 'digital comics'
            },
            {
                imgPath: 'merchandise.png',
                url: '#',
                text: 'merchandaise'
            },
            {
                imgPath: 'shop-locator.png',
                url: '#',
                text: 'shop locator'
            },
            {
                imgPath: 'subscriptions.png',
                url: '#',
                text: 'subscription'
            },
            {
                imgPath: 'dc-power-visa.svg',
                url: '#',
                text: 'DC POwer Visa'
            },
        ]
            }
        },
        methods: {
            getImagePath: function(imgPath){
                return new URL(imgPath, import.meta.url).href;
            }
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
    a{
        @include d-flex;
        justify-content: center;
        align-items: center;
        text-decoration: none;
        color: $white;
        span{
            text-align: left;
        }
        div.image {
            text-align: center;
            height: 100%;
            img {
                width: 50%;
                // margin-right: 1rem;
            }
            img[src*="svg"]{
                width: 80px;
                margin: 1rem;
            }
        }
        
    }
}
</style>