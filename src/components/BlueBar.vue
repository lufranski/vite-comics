<script>
    export default {
        data(){
            return{
                blueLinks: [
                    {
                        title: 'DIGITAL COMICS',
                        url: '#',
                        img: 'buy-comics-digital-comics.png'
                    },
                    {
                        title: 'DC MERCHANDISE',
                        url: '#',
                        img: 'buy-comics-merchandise.png'
                    },
                    {
                        title: 'SUBSCRIPTIONS',
                        url: '#',
                        img: 'buy-comics-subscriptions.png'
                    },
                    {
                        title: 'COMIC SHOP LOCATOR',
                        url: '#',
                        img: 'buy-comics-shop-locator.png'
                    },
                    {
                        title: 'DC POWER VISA',
                        url: '#',
                        img: 'buy-dc-power-visa.svg'
                    },
                ]
            }
        },
        methods: {
        getImagePath: function (imgPath) {
            return new URL(imgPath, import.meta.url).href;
        }
    }
    }
</script>

<template>
    <div>
        <div class="container">
            <ul>
                <li v-for="(blue, index) in blueLinks" :key="index">
                    
                    <a :href="blue.url">
                        <img :src="getImagePath(`../assets/images/${blue.img}`)" alt="">
                        <h4>
                            {{blue.title}}
                        </h4>
                    </a>
                </li>
            </ul>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;

    div {
        background-color: $primary;
        padding: 30px;

        .container {
            padding: 2rem 6rem;
        }
        ul {
            display: flex;
            flex-direction: row;
            justify-content: space-around;

            li {
                
                a {
                    color: #fff;
                    font-size: 12px;

                    img {
                        vertical-align: middle;
                        width: 30px;
                        height: 40px;
                        margin-right: .4rem;
                        object-fit: contain;
                    }

                    h4 {
                        display: inline-block;
                    }
                }
            }        
        }
    }
</style>
