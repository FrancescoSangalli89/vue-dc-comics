<template>
    <a href="#" class="product-card">
        <img :src="thumb" />
        <h3>{{series}}</h3>
    </a>
</template>

<script>

export default {
    name: "SingleProduct",
    props: {
        thumb: String,
        series: String
    }
}
</script>

<style lang="scss">
    .product-card {

        flex-basis: 15%;
        padding: 10px;
        margin-bottom: 1rem;
        text-align: center;
        margin: auto;
        text-decoration: none;

        img {
            max-width: 100%;
            margin-bottom: 1rem;
            object-fit: cover;
        }

        h3 {
            font-size: 12px;
            color: #fff;
        }

    }
</style>