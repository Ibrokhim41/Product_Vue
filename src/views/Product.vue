<template>
    <div class="product">
        <ProductGallery />
        <ProductInfo />
    </div>
</template>

<script>
import ProductInfo from '../components/ProductInfo'
import ProductGallery from '../components/ProductGallery'


export default {
    components: {
        ProductInfo,
        ProductGallery
    }
}
</script>

<style>
.product {
    display: flex;
    height: 100%;
}
</style>