<template>
    <div class="product-gallery">
        <div class="products">
            <button>
                <img src="../assets/Product-card/up.svg" alt="">
            </button>
            <div 
                class="products-img" 
                v-for="product in products" :key="product"
                @click="productView(product)"
            >
                <img :src="product" alt="">
            </div>
            <button>
                <img src="../assets/Product-card/down.svg" alt="">
            </button>
        </div>
        <div class="main-product">
            <img :src="mainProduct" alt="">
        </div>
    </div>
</template>

<script>
export default {
    name: 'ProductGallery',
    data() {
        return {
            products: ['https://cdn.shopify.com/s/files/1/0238/6181/files/2020-42mm-WHT3_1024x1024@2x.progressive.jpg?v=1601922616','https://staticimg.titan.co.in/Titan/Catalog/1785NL01_2.jpg', 'https://cdn.tmobile.com/content/dam/t-mobile/en-p/cell-phones/apple/Apple-iPhone-12/Blue/Apple-iPhone-12-Blue-thumbnail.png  ','https://www.vodafone.com.au/images/devices/samsung/samsung-galaxy-s21/samsung-galaxy-s21-plus-violet-front-m.jpg', 'https://lh3.googleusercontent.com/oUcqqJKN83HCa7ptJqZhy6vRYIsiISpXMoOqUtJ6xqsNNGpuU5B9G8gy87vP5IO1MfNtzbFfqtAan7ujMkekAegMVDJfUi9qwPhXYLU7gJ3HG-EbyEQcVmU=s512-c', 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR3VcuA3XfwYkh0WPXkamtD2y5bqstN_fO2pw&usqp=CAU'],
            mainProduct: 'https://lh3.googleusercontent.com/uq1pvz6hVro3CqeCGQlRWryafZiu-OLL1vuBCbcHmscIxAiOU2nUzDrY3WJe2XWNOgY4rLnJi7TgmcFGC12lyCP9jyfP8Ji3o-hpPPUDvDm6iMIAhrxjdg8XXAGIfyNyEUY9g_I=s512-c'

        }
    },
    methods: {
        productView(e) {
            this.mainProduct = e
        }
    }
}
</script>

<style>
.product-gallery {
    width: 50%;
    margin-right: 15px;
    display: flex;
}
.products {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-right: 16px;
}
.products button {
    background: #fff;
    border: 1px solid #E0E0E0;
    border-radius: 4px;
    cursor: pointer;
    padding: 6px;
    display: flex;
    justify-content: center;
    align-items: center;
    filter: drop-shadow(0px 2px 5px rgba(40, 41, 61, 0.1));
}
.products-img {
    display: flex;
    justify-content: center;
    align-items: center;
    border: 1px solid #E0E0E0;
    border-radius: 4px;
    padding: 3px 17px;
    margin: 12px 0;
    cursor: pointer;
}
.products-img  img {
    width: 30px;
    height: 58px;
    object-fit: contain;
}
.main-product {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 100%;
    border: 1px solid #E0E0E0;
    border-radius: 4px;
}
.main-product img {
    width: 100%;
}
</style>