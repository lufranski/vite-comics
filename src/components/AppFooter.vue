<script>
    import BlueBar from './BlueBar.vue';
    
    export default {
        components: {
            BlueBar
        }, 
        data (){
            return {
                footerLinks1: [
                    {
                        title: 'DC COMICS',
                        texts: ['Characters', 'Comics', 'Movies', 'TV', 'Games', 'Collectibles', 'Videos', 'Fans', 'News', 'Shop']
                    },
                    {
                        title: 'SHOP',
                        texts: ['Shop DC', 'Shop DC Collectibles']
                    },
                ],
                footerLinks2: [
                    {
                        title: 'DC',
                        texts: ['Terms of use', 'Privacy Policy (New)', 'Ad Choices', 'Advertising', 'Jobs', 'Subscriptions', 'Talent Workshops', 'CPSC Certificates', 'Ratings', 'Shop Help', 'Contact Us']
                    }
                ],
                footerLinks3: [
                    {
                        title: 'SITES',
                        texts: ['DC', 'MAD Magazine', 'DC Kids', 'DC Universe', 'DC Power Visa']
                    }
                ]    
        
            }
        }
    }
</script>

<template>
    <footer>
        
        <BlueBar/>
        <div class="container">
            <div class="left">
                
                <div class="col">
                    
                    <ul v-for="(element, index) in footerLinks1" :key="index">
                        <h4 class="tit">{{element.title}}</h4>
                        <li v-for="(text, index) in element.texts" :key="index">
                            <a href="#">
                                {{element.texts[index]}}
                            </a>
                        </li>
                    </ul>

                </div>
                <div class="col">
                    <ul v-for="(element, index) in footerLinks2" :key="index">
                        <h4 class="tit">{{element.title}}</h4>
                        <li v-for="(text, index) in element.texts" :key="index">
                            <a href="#">
                                {{element.texts[index]}}
                            </a>
                        </li>
                    </ul>
                </div>
                <div class="col">
                    <ul v-for="(element, index) in footerLinks3" :key="index">
                        <h4 class="tit">{{element.title}}</h4>
                        <li v-for="(text, index) in element.texts" :key="index">
                            <a href="#">
                                {{element.texts[index]}}
                            </a>
                        </li>
                    </ul>
                </div>

            </div>
            
            <div class="inner">
    
            </div>
        </div>

        <div class="bottom">
            <div class="button">
                <a href="#">
                    SIGN-UP NOW!
                </a>
            </div>

            <div class="social">
                <h3>FOLLOW US</h3>

                <div class="icons">
                    <img src="../assets/images/footer-facebook.png" alt="">
                    <img src="../assets/images/footer-twitter.png" alt="">
                    <img src="../assets/images/footer-youtube.png" alt="">
                    <img src="../assets/images/footer-pinterest.png" alt="">
                    <img src="../assets/images/footer-periscope.png" alt="">
                </div>
            </div>
        </div>

    </footer>
</template>

<style lang="scss" scoped>
    footer {
        width: 100%;
        background-image: url('../assets/images/footer-bg.jpg');
        background-repeat: no-repeat;
        background-size: cover;
        // DEBUG
        // height: 400px;
    
        .container {
            display: flex;
            // DEBUG
            // height: 100%;
    
            .inner {
                background-image: url('../assets/images/dc-logo-bg.png');
                background-repeat: no-repeat;
                background-position: right;
                background-size: cover;
                // DEBUG
                width: 50%;
                // height: 100%;
            }
            .left {
                width: 50%;
                display: flex;
                padding: 30px 0;
                
                .col {
                    width: calc(100% / 3);

                    .tit {
                        color: #fff;
                    }

                    a {
                        color: grey;
                        font-size: 10px;
                    }
                }
            
            }
        }
        .bottom {
            width: 100%;
            background-color: #303030;
            height: 100px;
            z-index: 200;
            display: flex;
            justify-content: space-around;
            align-items: center;

            .button {
                border: 1px solid #0282f9;
                width: 20%;
                padding: 15px;

                a {
                    color: #fff;
                }
            }

            .social {
                width: 50%;
                display: flex;

                h3 {
                    color: #0282f9;
                    margin-right: 20px;
                }

                .icons {
                    width: 60%;

                    img {
                        // vertical-align: middle;
                        margin-right: 10px;
                    }
                }

            }        
        }
    }



</style>