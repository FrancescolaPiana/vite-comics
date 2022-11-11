<template>
   <header>
   <div class="container" >
    <a href="">
    <img src="../assets/img/dc-logo.png" alt="">
    </a>
    <ul>
    <li v-for="(label,index) in labels" :key="index">
        <a :href="label.url" :class="{'active' : label.current}"> {{label.text}} </a>
    </li>
    </ul>
   </div>
   </header>
</template>

<script>
    export default {
        name: 'HeaderC',
        data() {
            return {
                labels: [
                {
                    text: "CHARACTERS",
                    url: "#",
                    current: false,
                },
                {
                    text: "COMICS",
                    url: "#",
                    current: true,
                },
                {
                    text: "MOVIE",
                    url: "#",
                    current: false,
                },
                {
                    text: "TV",
                    url: "#",
                    current: false,
                },
                {
                    text: "GAMES",
                    url: "#",
                    current: false,
                },
                {
                    text: "COLLECTIBLES",
                    url: "#",
                    current: false,
                },
                {
                    text: "VIDEOS",
                    url: "#",
                    current: false,
                },
                {
                    text: "FANS",
                    url: "#",
                    current: false,
                },
                {
                    text: "NEWS",
                    url: "#",
                    current: false,
                },
                {
                    text: "SHOP",
                    url: "#",
                    current: false,
                },
            ]
            }
        },
    }
</script>

<style lang="scss" scoped>
// i declare the files where i will take my prefix
@use '../styles/partials/variables' as *;
@use '../styles/partials/mixins' as *;

    header{
        padding: 0.5rem 0rem ;
            .container{
            max-width: 1170px;
            margin: 0 auto ;
            display: flex;
            align-items: center;
            justify-content: space-between;
            }
        ul{
            list-style: none;
            // margin: 2.5rem 1rem 5rem;
            display: flex;
            justify-content: end;
            li a{
                display: flex;
                margin: 1rem;
                text-decoration: none;
                font-size: 0.6em;
                transform: scale(1,1.8);
                font-weight: 700;
                color: $lightgrey;
                border-bottom: 2px solid rgba(255, 255, 255, 0);
                height: 68px;
                justify-content: center;
                align-items: center;

                &.active, &:hover{
                    border-bottom:  2px solid $blue;
                    color: $darkgrey;
                }
            }
        }
    }

</style>