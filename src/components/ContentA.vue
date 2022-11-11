<template>
    <div class="principal">
        <div class="container">
            <a class="card" href=""> 
                <div class="cropped">
                    <img :src="products[0].thumb" alt="" class="thumb">
                </div>
                <h3 class="series">{{products[0].series}}</h3>
                <h5 class="price">{{products[0].price}}</h5>
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
            .card{
                width: 250px;
                background-color: $black;
                display: flex;
                flex-direction: column;
                align-items: center;
                padding: 30px;
                border-radius: 15px;
                transition: background-color, padding 250ms ;
                text-decoration: none;
                
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
                    width: 192px;
                    height: 192px;
                    display: flex;
                    align-items: center ;
                    overflow: hidden;
                    border-radius: 5px;
                    background-color: aliceblue;
                    margin-bottom: 20px; 
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
                        margin-bottom: -98px; 
                        transition: all 250ms;
                    }
                }
                .series{
                    display: inline-block;
                    color: $lightgrey;
                    font-weight: 400;
                    text-transform: uppercase;
                    font-size: 0.9rem;
                    align-self: flex-start;
                    margin-bottom: 8px;
                    transition: color 200ms;
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