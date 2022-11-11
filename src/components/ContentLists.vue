<template>
    <div>
        <div class="principal">
        <div class="container">
            <ul>
            <h3>dc comics</h3>
            <li v-for="(list,i) in labels" :key="i">
                <a :href="list.url">
                    <span>{{list.text}}</span>
                </a>
            </li>
            </ul>
            
            <ul>
            <h3>shop</h3>
            <li v-for="(list,i) in labels2" :key="i">
                <a :href="list.url">
                    <span>{{list.text}}</span>
                </a>
            </li>
            </ul>

            <ul>
            <h3>dc</h3>
            <li v-for="(list,i) in labels3" :key="i">
                <a :href="list.url">
                    <span>{{list.text}}</span>
                </a>
            </li>
            </ul>
            <ul>
            <h3>sites</h3>
            <li v-for="(list,i) in labels4" :key="i">
                <a :href="list.url">
                    <span>{{list.text}}</span>
                </a>
            </li>
            </ul>

        <div class="img">
            <img src="../assets/img/dc-logo-bg.png" alt="">
        </div>

        </div>
    </div>
    </div>
</template>

<script>
    export default {
        name: 'ContentLists',
        data() {
            return {
                labels: [
                {
                    text: "Characters",
                    url: "#",
                },
                {
                    text: "Comics",
                    url: "#",
                },
                {
                    text: "Movie",
                    url: "#",
                },
                {
                    text: "Tv",
                    url: "#",
                },
                {
                    text: "Games",
                    url: "#",
                },
                {
                    text: "Videos",
                    url: "#",
                },
                {
                    text: "News",
                    url: "#",
                },
                ],

            labels2: [
                {
                    text: "Shop DC",
                    url: "#",
                },
                {
                    text: "Shop DC Collectibles",
                    url: "#",
                },
            ],

            labels3: [
                {
                    text: "Term Of Use",
                    url: "#",
                },
                {
                    text: "Privacy policy (New)",
                    url: "#",
                },
                {
                    text: "Ad Choices",
                    url: "#",
                },
                {
                    text: "Advrtise",
                    url: "#",
                },
                {
                    text: "Jobs",
                    url: "#",
                },
                {
                    text: "Subscriptions",
                    url: "#",
                },
                {
                    text: "Talent Workshops",
                    url: "#",
                },
                {
                    text: "CPSC Certificates",
                    url: "#",
                },
                {
                    text: "Ratings",
                    url: "#",
                },
                {
                    text: "Shop Help",
                    url: "#",
                },
                {
                    text: "Contact Us",
                    url: "#",
                },
            ],
            labels4: [
                {
                    text: "DC",
                    url: "#",
                },
                {
                    text: "MAS Magazine",
                    url: "#",
                },
                {
                    text: "DC Kids",
                    url: "#",
                },
                {
                    text: "DC Universe",
                    url: "#",
                },
                {
                    text: "DC Power Visa",
                    url: "#",
                },
            ],
            }
        },
    }
</script>

<style lang="scss" scoped>

    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;
    .principal{
        background-image: url(../assets/img/footer-bg.jpg);
        background-size: cover;
        background-position: top;
        padding: 3rem 0rem;
        overflow: hidden;
        
        .container{
            max-width: 1170px;
            margin: 0 auto ;
            position: relative;
            display: flex;
            flex-direction: column;
            flex-wrap: wrap;
            height: 300px;
            justify-content: space-between;
            padding-right: 700px;
            
            .img{
                img{
                position: absolute;
                top: -150px;
                right: 0;
                }
            }
            
            ul{
                display: inline-block;
                list-style: none;
                margin-bottom: 20px;
                h3{
                    transform: scale(1,1.5);
                    font-size: 0.8rem;
                    display: inline-block;
                    color: $white;
                    margin-bottom: 5px;
                    text-transform: uppercase;
                }
                li a{
                    display: inline-block;
                    text-decoration: none;
                    color: $lightgrey;
                    font-weight: 400;
                    font-size: 0.8rem;
                    margin-bottom: 3px;
                    &:hover{
                    color: $white;
                    }
                }
            }
        }

    }
</style>