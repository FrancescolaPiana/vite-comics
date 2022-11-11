<template>
    <div class="principal">
        <div class="container">
            <div class="labs">
                <span>current series</span>
            </div>
            <a class="card" href="" v-for="(card,i) in products" :key="i" > 
                <div class="cropped">
                    <img :src="card.thumb" :alt="card.series" class="thumb">
                </div>
                <div class="text">
                    <h3 class="series">{{card.series}}</h3>
                    <h5 class="price">{{card.price}}</h5>
                </div>
            </a>
        </div>
    </div>
</template>

<script>
    import {comics} from '../data/dc-comics';
    export default {
        name: 'ContentA',
        data() {
            return {
                products: comics
            }
        },
        mounted() {
            console.log(this.products)
        },
    }
</script>

<style lang="scss" scoped>
    @use '../styles/partials/variables' as *;
    @use '../styles/partials/mixins' as *;

    @keyframes pulse {
        0%{
            transform: scale(0.98);
        }
        40%{
            transform: scale(1);
        }
        100%{
            transform: scale(0.98);
        }
    }

    @keyframes flips {
        0%{
            transform: rotateY(0deg);
        }
        50%{
            transform: rotateY(90deg);
        }
        100%{
            transform: rotateY(0deg);
        }
    }

    .principal{
        background-color: $darkgrey;
        padding: 3rem 0rem;
        .container{
            max-width: 1170px;
            margin: 0 auto ;
            display: flex; gap: 15px;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: center;
            position: relative;
            .labs{
                position: absolute;
                top: -80px;
                z-index: 100;
                background-color: $blue;
                padding: 1em 2em;
                span{
                    display: inline-block;
                    font-size: 1.5em;
                    text-transform: uppercase;
                    color: $white;
                    font-weight: 900;
                    transform: scale(0.9,1.1);
                }
            }
            .card{
                width: 180px;
                height: 260px;
                background-color: $black;
                display: flex;
                flex-direction: column;
                align-items: center;
                padding: 12px;
                border-radius: 15px;
                transition: background-color, padding 250ms ;
                text-decoration: none;
                justify-content: space-between;
                
                &:hover{
                    background-color: $grey;
                    box-shadow: 0px 5px 5px rgba(0, 0, 0, 0.5);
                    animation: pulse 1200ms infinite;
                    .cropped{
                     
                        // animation: flips 4000ms infinite;

                        .thumb{
                          
                        }
                    }
                    .series{
                        color: $white;
  
                    }
                    .price{
                        color: $white;

                    }
                }
                .cropped{
                    width: 150px;
                    height: 160px;
                    display: flex;
                    align-items: center ;
                    overflow: hidden;
                    border-radius: 5px;
                    background-color: aliceblue;
                    margin-bottom: 0px; 
                    position: relative;
                    
                    .hid1{
                        // display: none;
                        z-index: 1000;
                        position: absolute;
                        color: $white;
                    }
                    .hid2{
                        // display: none;
                        z-index: 1000;
                        position: absolute;
                        color: $white;
                        left: 0px;
                    }
                    .thumb{
                        margin-bottom: -68px; 
                        // margin-left: -15px;
                        width: 150px;
                        transition: all 250ms;
                    }
                }
                .text{
                    display: flex;
                    flex-direction: column;
                    align-self: flex-start;
                }
                .series{
                    display: inline-block;
                    color: $lightgrey;
                    font-weight: 400;
                    text-transform: uppercase;
                    font-size: 0.9rem;
                    align-self: flex-start;
                    transition: color 200ms;
                    overflow: hidden;
                    max-height: 40px;
                }
                .price{
                    display: inline-block;
                    color: $lightgrey;
                    font-weight: 400;
                    text-transform: uppercase;
                    font-size: 1.5rem;
                    align-self: flex-start;
                    transition: color 200ms;
                }
            }
        }
    }
</style>