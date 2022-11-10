<template>
    <div>
        <div class="container">
            <ul>
               <li>DCCOMICS</li>    
               <li>DCCOMICS</li>    
               <li>DCCOMICS</li>    
               <li>DCCOMICS</li>    
               <li>DCCOMICS</li>    
               <li>DCCOMICS</li>    
              
            </ul>
            <ul>
                <li>ciao</li>
                <li>ciao</li>
                <li>ciao</li>
                <li>ciao</li>
                <li>ciao</li>
            </ul>
            <ul>
                <li>ciao</li>
                <li>ciao</li>
                <li>ciao</li>
                <li>ciao</li>
                <li>ciao</li>
            </ul>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'FooterComponent',
        data() {
            return {
                sections: [
                    [
                        {
                           title: 'dccomics',
                           links: [
                            'characters',
                            'comics',
                            'tv',
                            'movies',
                            'collectivbles',
                            'videos',
                            'fans'
                           ]
                        },
                        {
                           title: 'dccomics',
                           links: [
                            'characters',
                            'comics',
                            'tv',
                            'movies',
                            'collectivbles',
                            'videos',
                            'fans'
                           ]
                        }
                    
                    ],
                    [
                        'dc'
                    
                    ],
                    [
                        'site',
                    ]

                    
                    ]
            }
        },
    }
</script>

<style lang="scss" scoped>
@use '../assets/style/partials/mixins' as *;
@use '../assets/style/partials/variables' as *;
div {
    background-color: $almost-dark;
    background-image: url('../assets/img/footer-bg.jpg');
    div.container {
        @include d-flex;
        ul {
            list-style: none;
            padding: 1rem;
            color: $grey;
            &:first-child{
                color: $white;
            }
        }
    }

}

</style>