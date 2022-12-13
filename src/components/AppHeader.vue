<script>
    export default {
        data(){
            return{
                activeLink: 0,
                links: [
                    {
                        title: 'CHARACTERS',
                        url: '#',
                        current: false
                    },
                    {
                        title: 'COMICS',
                        url: '#',
                        current: true
                    },
                    {
                        title: 'MOVIES',
                        url: '#',
                        current: false
                    },
                    {
                        title: 'TV',
                        url: '#',
                        current: false
                    },
                    {
                        title: 'GAMES',
                        url: '#',
                        current: false
                    },
                    {
                        title: 'COLLECTIBLES',
                        url: '#',
                        current: false
                    },
                    {
                        title: 'VIDEOS',
                        url: '#',
                        current: false
                    },
                    {
                        title: 'FANS',
                        url: '#',
                        current: false
                    },
                    {
                        title: 'NEWS',
                        url: '#',
                        current: false
                    },
                    {
                        title: 'SHOP',
                        url: '#',
                        current: false
                    }
                ]
            }
        },
        // methods : {
        //     toggleActive (indice){
                                    
        //         this.links[indice].current = true;

        //     }
        // }
    }
</script>

<template>
    <header>
        <div class="container">

            <a href="/" class="brand">
                <img src="../assets/images/dc-logo.png" alt="">
            </a>
    
            <nav>
    
                <ul>
                    <li v-for="(link, index) in links" :key="index">
                        <a :class="{active: link.current}" :href="link.url">
                            {{link.title}}
                        </a>
                    </li>
                </ul>
            
            </nav>

        </div>

    </header>
</template>

<style lang="scss" scoped>
@use '../styles/partials/variables' as *;


header {
    width: 100%;
    position: fixed;
    background-color: #fff;
    z-index: 200;
    // padding: 5px 0;
    
    .container {
        width: 80%;
        display: flex;
        justify-content: space-between;

        img {
            width: 60%;
        }

        nav {
            width: 60%;

            ul {    
                display: flex;
                flex-direction: row;
                width:  100%;
                padding-top: 20px;
        
                a {
                    color: #515b68;
                    font-size: 12px;
                    font-weight: bold;
                    margin-right: 1rem;
                    padding: 25px 10px;

                    &:hover {
                        color: $primary;
                        border-bottom: 4px solid $primary;            
                    }    
                }
            }
        }
        .active {
            color: $primary;
            border-bottom: 4px solid $primary;
        }
    }

}

</style>
