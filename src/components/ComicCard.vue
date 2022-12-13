<script>
export default {
    props: {
        item: Object
    }
}
</script>

<template>
    <div class="card">
        <a href="#">
            <img :src="item.thumb" alt="item.type">
    
            <h4>{{item.series}}</h4>
        </a>
    </div>
</template>

<style lang="scss" scoped>

    .card {
        width: calc((100% / 6) - 1rem);

        a {
            color: #fff;
            
            h4 {
                font-size: 8px;
            }
        }
    }
    
</style>