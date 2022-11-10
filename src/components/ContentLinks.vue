<template>
    <div class="principal">
        <div class="container">
            <ul>
            <li v-for="(link,i) in links" :key="i">
                <a :href="link.url">
                    <img :src="link.img" alt="">
                    <h3>{{link.text}}</h3>
                </a>
            </li>
            </ul>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'ContentLinks',
        data() {
            return {
                links: [
                {
                    text: "DIGITAL COMICS",
                    url: "#",
                    img: "../assets/img/buy-comics-digital-comics.png"
                },
                {
                    text: "DC MERCHANDISE",
                    url: "#",
                    img: "../assets/img/buy-comics-merchandise.png"
                },
                {
                    text: "SUBSCRIPTION",
                    url: "#",
                    img: "../assets/img/buy-comics-subscriptions.png"
                },
                {
                    text: "COMIC SHOP LOCATOR",
                    url: "#",
                    img: "../assets/buy-comics-shop-locator.png"
                },
                {
                    text: "DC POWER VISA",
                    url: "#",
                    img: "../assets/img/buy-dc-power-visa.svg"
                },
            ]
            }
        },
    }
</script>

<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;

    .principal{
        background-color: $blue;
        padding: 3rem 0rem;
        .container{
            max-width: 1170px;
            margin: 0 auto ;
            ul{
            list-style: none;
            display: flex;
            justify-content: space-between;
                li a{
                    text-decoration: none;
                    display: flex;
                    margin: 1rem;
                    color: white;
                }
            }
        }
    }
</style>