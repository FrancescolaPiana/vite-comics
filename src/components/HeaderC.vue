<template>
   <header>
   <div class="container" >
    <a href="">
    <img src="../assets/img/dc-logo.png" alt="">
    </a>

    <ul>
    <li v-for="(label,index) in labels" key="index">
        <a :href="labels.url"> {{labels[index].text}} </a>
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
        padding: 1rem 0;
            .container{
            max-width: 1170px;
            margin: 0 auto ;
            display: flex;
            align-items: center;
            justify-content: space-between;
            }
        ul{
            list-style: none;
            margin: 2.5rem 1rem 5rem;
            @include dFlex;
            

            li a{
                display: inline-block;
                padding: 1rem;
                text-decoration: none;
            }
        }
    }

</style>