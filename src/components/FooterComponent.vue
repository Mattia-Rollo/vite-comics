<template>
    <div class="wrapper">
        <div class="container">
            <ul>
                <ul>
                    <li v-for="(item, index) in comics" :key="index">
                        <a :href="item.url">{{ item.linkText }}</a>
                    </li>
                </ul>

                <ul>
                    <li v-for="(item, index) in shop" :key="index">
                        <a :href="item.url">{{ item.linkText }}</a>
                    </li>
                </ul>
            </ul>
            <ul>
                <li v-for="(item, index) in dc" :key="index">
                    <a :href="item.url">{{ item.linkText }}</a>
                </li>
            </ul>
            <ul>
                <li v-for="(item, index) in sites" :key="index">
                    <a :href="item.url">{{ item.linkText }}</a>
                </li>
            </ul>
            <div class="logo"></div>
        </div>
    </div>
</template>

<script>
export default {
    name: "FooterComponent",
    data() {
        return {
            comics: [
                {
                    linkText: "Dc Comics",
                    url: "#",
                },
                {
                    linkText: "Characters",
                    url: "#",
                },
                {
                    linkText: "Comics",
                    url: "#",
                },
                {
                    linkText: "Movies",
                    url: "#",
                },
                {
                    linkText: "TV",
                    url: "#",
                },
                {
                    linkText: "Games",
                    url: "#",
                },
                {
                    linkText: "Videos",
                    url: "#",
                },
                {
                    linkText: "News",
                    url: "#",
                },
            ],
            shop: [
                {
                    linkText: "Shop",
                    url: "#",
                },
                {
                    linkText: "Shop DC",
                    url: "#",
                },
                {
                    linkText: "Shop DC Collectables",
                    url: "#",
                },
            ],
            dc: [
                {
                    linkText: "Terms Of Use",
                    url: "#",
                },
                {
                    linkText: "Privacy Policy",
                    url: "#",
                },
                {
                    linkText: "Ad Choices",
                    url: "#",
                },
                {
                    linkText: "Advertising",
                    url: "#",
                },
                {
                    linkText: "Jobs",
                    url: "#",
                },
                {
                    linkText: "Subscriptions",
                    url: "#",
                },
                {
                    linkText: "Talent Workshops",
                    url: "#",
                },
                {
                    linkText: "CPSC Certificates",
                    url: "#",
                },
                {
                    linkText: "Ratings",
                    url: "#",
                },
                {
                    linkText: "Shop Help",
                    url: "#",
                },
                {
                    linkText: "Contact Us",
                    url: "#",
                },
            ],
            sites: [
                {
                    linkText: "DC",
                    url: "#",
                },
                {
                    linkText: "MAD Magazine",
                    url: "#",
                },
                {
                    linkText: "DC Kids",
                    url: "#",
                },
                {
                    linkText: "DC Universe",
                    url: "#",
                },
                {
                    linkText: "DC Power Visa",
                    url: "#",
                },
            ],
        };
    },
};
</script>

<style lang="scss" scoped>
@use '../assets/style/partials/mixins' as *;
@use '../assets/style/partials/variables' as *;

.wrapper {
    position: relative;
    background-color: $almost-dark;
    background-image: url("/img/footer-bg.jpg");
    background-repeat: no-repeat;
    background-size: cover;
    overflow: hidden;
}

div.container {
    @include d-flex;
    padding: 1rem 0;

    // background: transparent;s
    ul {
        margin: 0;
        list-style: none;
        padding: 0 1.2rem 1rem 0;
        color: $grey;

        li a {
            text-decoration: none;
            padding: 5px 0;
            color: $grey;
            display: inline-block;
            padding: 0.2rem 0;
        }

        li:first-child a {
            display: inline-block;
            text-transform: uppercase;
            color: $white;
            font-size: 1.2rem;
            padding: 1rem 0;
        }
    }
}

.logo {
    background-image: url("../assets/img/dc-logo-bg.png");
    background-color: transparent;
    position: absolute;
    right: 0;
    top: 50%;
    transform: translateY(-50%);
    margin-left: auto;
    width: 500px;
    height: 500px;
}
</style>
