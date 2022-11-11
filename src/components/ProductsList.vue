<template>
    <div>
        <div class="container">
            <div>CURRENT SERIES</div>
            <h1>Content goes here</h1>
        </div>
    </div>
</template>

<script>
export default {
    name: 'ProductsList',
    data() {
        return {

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
        div:first-child{
            position: absolute;
            top: -2.5rem;
            padding: 1rem;
            background-color: $blue;
            font-weight: 700;

        }
    }
}

</style>