<script>
export default {
    props: {
        item: Object
    }
}
</script>

<template>
    <div class="card">
        <img :src="item.thumb" alt="item.type">

        <h4>{{item.series}}</h4>
    </div>
</template>

<style lang="scss" scoped>

    .card {
        width: calc((100% / 6) - 1rem);

        h4 {
            font-size: 8px;
        }
    }
</style>