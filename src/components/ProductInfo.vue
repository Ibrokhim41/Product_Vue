<template>
    <div class="product-info">
        <div class="top">
            <div class="title">100% органический 10 лет корень корейского женьшеня красный Panax улучшить иммунную</div>
        <div class="star-rating">
            <star-rating 
                :rating='3.5'
                :increment='0.5'
                :read-only="true"
                :star-size="18" 
                :inactive-color="'#ffffff'" 
                :active-color="['#DAD873','#DAD873']"
                :border-color="'#DAD873'" 
                :show-rating="false"
                :border-width="1"
                :rounded-corners="true" 
                :padding="6">
            </star-rating>
            <span>254</span>
            <p>Количество заказов: 1</p>
        </div>
        </div>
        <div class="main-top">
            <div class="price">
                <div class="price-curent">15 000 000 сум</div>
                <div class="discount">
                    <div class="price-old">20 000 000 сум</div>
                    <span>-25%</span>
                </div>
            </div>
            <div class="payment">
                <p>Методы оплаты:</p>
                <div class="payment-methods">
                    <img src="../assets/Product-card/Payme.svg" alt="">
                    <img src="../assets/Product-card/Humo.svg" alt="">
                    <img src="../assets/Product-card/Click.svg" alt="">
                </div>
            </div>
            <div class="delivery">
                <p>Методы доставки:</p>
                <div class="delivery-methods">
                    <div>
                        <img src="../assets/Product-card/ad-product.svg" alt="">
                        Доставка продавца
                    </div>
                    <div>
                        <img src="../assets/Product-card/delivery.svg" alt="">
                        Самовывоз
                    </div>
                </div>
            </div>
        </div>
        <div class="main-bottom">
            <p>Количество</p>
            <div class="counter">
                <button @click="() => product > 0 && product--">
                    <img src="../assets/Product-card/minus.svg" alt="">
                </button>
                <input type="text" v-model="product">
                <button @click="() => product++">
                    <img src="../assets/Product-card/plus.svg" alt="">
                </button>
                <div class="available">
                    <img src="../assets/Product-card/Fill.svg" alt="">
                    в наличии 1 245  шт.
                </div>
            </div>
            <div class="buy">
                <button class="buy-button">Купить в один клик</button>
                <button class="partner-button">Связаться с продавцом</button>
            </div>
        </div>
        <div class="bottom">
            <p>* Стоимость доставки заказов до 40 000 сум  - договорная</p>
            <p>** Бесплатная доставка при заказе от 40 000 сум</p>
        </div>
    </div>
</template>

<script>
import StarRating from 'vue-star-rating'

export default {
    data() {
        return {
            rating: null,
            product: 0,
        }
    },
    name: 'ProductInfo',
    components: {StarRating},
    methods: {
    }
}
</script>

<style>
.product-info {
    width: 50%;
    margin-left: 15px;
}
.top {
    border-bottom: 1px solid #E1DFDF;
    padding-bottom: 30px;
}
.title {
    font-size: 20px;
    font-weight: 500;
    color: #2F323D;
}
.star-rating {
    display: flex;
    align-items: center;
    margin-top: 14px;
}
.star-rating span {
    margin-left: 8px;
    font-size: 11px;
    color: #596178;
}
.star-rating p {
    margin-left: 48px;
    font-size: 11px;
    color: #596178;
}

/* main-top */
.main-top {
    padding: 24px 0 20px;
    border-bottom: 1px solid #E1DFDF;
}
.price-curent {
    font-size: 24px;
    font-weight: 500;
    color: #2F323D;
    margin-bottom: 11px;
}
.discount {
    display: flex;
    align-items: center;
}
.discount span {
    font-size: 13px;
    color: #FFFFFF;
    background: #FF5530;
    border-radius: 6px;
    padding: 2px 5px;
    margin-left: 25px;
}
.price-old {
    font-size: 13px;
    color: #596178;
    text-decoration: line-through;
}

/* payment */
.payment {
    display: flex;
    align-items: center;
    margin-top: 16px;
}
.payment p {
    font-size: 13px;
    color: #596178;
}
.payment-methods {
    margin-left: 8px;
}
.payment-methods img {
    width: 50px;
    height: auto;
    margin-right: 16px;
    cursor: pointer;
}

/* delivery */
.delivery {
    display: flex;
    align-items: center;
    margin-top: 16px;
}
.delivery p {
    font-size: 13px;
    color: #596178;
}
.delivery-methods {
    display: flex;
    margin-left: 17px;
}
.delivery-methods div {
    display: flex;
    align-items: center;
    margin-right: 20px;
    font-size: 13px;
    color: #2F323D;
    cursor: pointer;
}
.delivery-methods img {
    width: 24px;
    height: 24px;
    margin-right: 10px;
}

/* main-bottom */
.main-bottom {
    padding: 15px 0 24px;
    border-bottom: 1px solid #E1DFDF;
}
.main-bottom p {
    font-size: 13px;
    color: #2F323D;
}

/* counter */
.counter {
    display: flex;
    align-items: center;
    margin: 14px 0 33px;
}
.counter button {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 42px;
    height: 42px;
    background: #fff;
    border: 1px solid #E0E0E0;
    border-radius: 4px;
    cursor: pointer;
}
.counter input {
    background: #F6F6F6;
    border: 1px solid #E0E0E0;
    border-radius: 4px;
    width: 60px;
    height: 42px;
    margin: 0 8px;
    text-align: center;
    font-size: 17px;
    color: #2F323D;
}
.counter input:focus {
    outline: none;
}
/* available */
.available {
    display: flex;
    align-items: center;
    background: #EFEEB4;
    border-radius: 4px;
    font-size: 11px;
    color: #596178;
    padding: 2px 8px 0 0;
    margin-left: 20px;
}
.available img {
    width: 35px;
    height: auto;
    margin-right: 16px;
}

/* buy */
.buy button{
    border: 1px solid #E0E0E0;
    border-radius: 4px;
    font-size: 17px;
    padding: 8px 32px;
    cursor: pointer;
}
.buy-button {
    color: #fff;
    background: #309975;
}
.partner-button {
    background: #fff;
    color: #2F323D;
    margin-left: 16px;
}
.bottom {
    padding-top: 16px;
    font-size: 15px;
    color: #596178;
}
</style>