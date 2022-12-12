<script>
    export default {
        
    }
</script>

<template>
    <header>
        <a href="/" class="brand">
            <img src="../assets/images/dc-logo.png" alt="">
        </a>

        <nav>

            <ul>
                <li>
                    <a href="#">
                        Characters
                    </a>
                </li>
                <li>
                    <a href="#">
                        Comics
                    </a>
                </li>
                <li>
                    <a href="#">
                        Movies
                    </a>
                </li>
                <li>
                    <a href="#">
                        TV
                    </a>
                </li>
            </ul>
        
        </nav>
    </header>
</template>

<style lang="scss" scoped>

header {
    display: flex;
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    justify-content: space-between;
    
    ul {
        list-style-type: none;
    
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        width:  40%;

        a {
            color: #515b68;
        }
    }
}

</style>
