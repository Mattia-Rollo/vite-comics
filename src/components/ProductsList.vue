<template>
    <div>
        <div class="container">
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
}

</style>