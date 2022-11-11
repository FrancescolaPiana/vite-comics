<template>
    <div class="principal">
        <div class="container">

           <div>
           <a class="button" href="">
                <span>sign-up now!</span>
            </a>
            </div>
            
            <div>
            <ul>
            <li><span>follow</span></li>
            <li v-for="(link,i) in socials" :key="i">
                <a class="socials" :href="link.url">
                    <img :id="`img${i}`" :src="getImagePath(`../assets/img/${link.img}`)" class="img-icon">
                    <span>{{link.text}}</span>
                </a>
            </li>
            </ul>
            </div>
           

            
        </div>
    </div>
</template>

<script>
    export default {
        name: 'FooterC',
        data() {
            return {
                socials: [
                {
                    img: "footer-facebook.png",
                    url: "#",
                },
                {
                    img: "footer-twitter.png",
                    url: "#",
                },
                {
                    img: "footer-youtube.png",
                    url: "#",
                },
                {
                    img: "footer-pinterest.png",
                    url: "#",
                },
                {
                    img: "footer-periscope.png",
                    url: "#",
                },
               
            ],
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
        padding: 2rem 0rem;
        background-color: $grey;
        height: 140px;
        .container{
            max-width: 1170px;
            height: 100%;
            margin: 0 auto ;
            position: relative;
            display: flex;
            justify-content: space-between;
            align-items: center;
            .button{
                border: 2px solid $blue;
                padding: 1rem;
                display: flex;
                justify-content: center;
                align-items: center;
                text-decoration: none;
                color: $white;
                text-transform: uppercase;
                transition: background-color 250ms;
                &:hover{
                    background-color: $blue;
                }
            }
            ul{
                list-style: none;
                display: flex;
                align-items: center;
                gap: 20px;
                li{
                    text-transform: uppercase;
                    span{
                        display: block;
                        color: $blue;
                        transform: scale(1,1.3);
                    }

                    .socials{
                        transition: filter 250ms ;
                        &:hover{
                            filter: brightness(1.5);
                        }
                    }
                }
            }

        }
        
    }
</style>