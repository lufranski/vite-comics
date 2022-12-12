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
        <nav>
            <ul>
                <li v-for="(blue, index) in blueLinks" :key="index">
                    <img :src="getImagePath(`../assets/images/${blue.img}`)" alt="">
                    
                    <a :href="blue.url">
                        {{blue.title}}
                    </a>
                </li>
            </ul>
        </nav>
    </div>
</template>

<style lang="scss" scoped>
    div {
        background-color: #0282f9;
        padding: 30px;

        nav {
            width: 80%;
            height: 100%;
            margin: 0 auto;
            padding: 0 50px;
        }
        ul {
            display: flex;
            flex-direction: row;

            li {
               margin-right: 35px;
                height: 50px;
                                
                img {
                    vertical-align: middle;
                    margin-right: 10px;
                    max-width: 40px;
                    min-height: 50px;
                }

                a {
                    color: #fff;
                    font-size: 12px;
                }
            }        
        }
    }
</style>
