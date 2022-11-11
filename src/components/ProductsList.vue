<template>
    <div>
        <div class="container">
            <div class="info">CURRENT SERIES</div>
            <div class="container">
                <div class="row">
                    <div v-for="(item,index) in comics" :key="index" class="card">
                        <a href="#">
                            <img :src="item.thumb" :alt="item.type">
                            <div>{{item.series}}</div>
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import {comics} from '../assets/data/data'
export default {
    name: 'ProductsList',
    data() {
        return {
            comics: comics
        }
    },
}
</script>

<style lang="scss" scoped>
@use '../assets/style/partials/mixins' as *;
@use '../assets/style/partials/variables' as *;

div {
    background-color: $black-bg-main;
    color: $white;
    padding: 1rem 0;
    
    div.container{
        position: relative;
        div.info{
            position: absolute;
            top: -2.5rem;
            padding: 1rem;
            background-color: $blue;
            font-weight: 700;

        }
        div.row{
            @include d-flex;
            flex-wrap: wrap;
            div.card{
                width: calc(100% / 6);
                padding: 0 1rem ;
                a{
                    text-decoration: none;
                }
                img{
                    height: 170px;
                    width: 100%;
                    object-fit: cover;
                    object-position: top;
                }
                div{
                    text-align: center;
                }
            }
        }
    }
}

</style>