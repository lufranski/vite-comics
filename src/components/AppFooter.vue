<script>
    import BlueBar from './BlueBar.vue';
    
    export default {
        components: {
            BlueBar
        }
    }
</script>

<template>
    <footer>
        
        <BlueBar/>
        <div class="container">
            <div class="left">
                <ul>
                    <li>
                        <a href="#">Characters</a>
                    </li>
                </ul>
            </div>
            
            <div class="inner">
    
            </div>
        </div>

        <div class="bottom"></div>

    </footer>
</template>

<style lang="scss" scoped>
    footer {
        width: 100%;
        background-image: url('../assets/images/footer-bg.jpg');
        background-repeat: no-repeat;
    }

    .container {
        display: flex;
    }
    .inner {
        background-image: url(../assets/images/dc-logo-bg.png);
        background-position: center;
        background-size: contain;
        background-repeat: no-repeat;
        // DEBUG
        width: 50%;
        height: 500px;
    }

    .left {
        width: 50%;
    }

    .bottom {
        width: 100%;
        background-color: #303030;
        height: 100px;
    }
</style>