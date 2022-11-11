<template>
    <div class="principal">
        <div class="container">
            <ul>
            <li v-for="(link,i) in links" :key="i">
                <a :href="link.url">
                    <img :id="`img${i}`" :src="getImagePath(`../assets/img/${link.img}`)" class="img-icon">
                    <span>{{link.text}}</span>
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
                    img: "buy-comics-digital-comics.png"
                },
                {
                    text: "DC MERCHANDISE",
                    url: "#",
                    img: "buy-comics-merchandise.png"
                },
                {
                    text: "SUBSCRIPTION",
                    url: "#",
                    img: "buy-comics-subscriptions.png"
                },
                {
                    text: "COMIC SHOP LOCATOR",
                    url: "#",
                    img: "buy-comics-shop-locator.png"
                },
                {
                    text: "DC POWER VISA",
                    url: "#",
                    img: "buy-dc-power-visa.svg"
                },
            ]
            }
        },

        methods: {
            getImagePath(imgPath){
                return new URL(imgPath, import.meta.url).href;
            }
        }
    }
</script>

<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;

    .principal{
        background-color: $blue;
        padding: 2rem 0rem;
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
                    align-items: center;
                    gap: 10px;
                    margin: 1rem;
                    color: $white;
                    font-weight: 400;
                    font-size: 0.8rem;
                    .img-icon{
                        height: 50px;
                    }
                    #img4{
                        width: 50px;
                    }
                }
            }
        }
    }
</style>