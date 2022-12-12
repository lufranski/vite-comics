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
        // DEBUG
        height: 400px;
    }

    .container {
        display: flex;
        // DEBUG
        height: 100%;
    }
    .inner {
        background-image: url(../assets/images/dc-logo-bg.png);
        background-size: contain;
        background-repeat: no-repeat;
        // DEBUG
        width: 50%;
        height: 100%;
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