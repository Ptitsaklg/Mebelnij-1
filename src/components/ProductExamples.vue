<script setup>
import Product from './Product.vue';
import { ref } from 'vue';

const products = ref([
    {
        id: 1,
        img: '/img/product-11.png',
        title: 'Шикарное кресло',
        price: 2550
    },
    {
        id: 2,
        img: '/img/product-12.png',
        title: 'Набор ваз в деревенском стиле',
        price: 1550
    },
    {
        id: 3,
        img: '/img/product-14.png',
        title: 'Шелковистая ваза',
        price: 1250
    },
    {
        id: 4,
        img: '/img/product-15.png',
        title: 'Лампа Люси',
        price: 3990
    },
])

</script>

<template>
    <div class="products">
        <Product
        v-for="product of products"
        :key="product.id"
        :img="product.img"
        :title="product.title"
        :price="product.price"
        >
        </Product>
    </div>
</template>

<style lang="sass" scoped>
@import '../assets/styles/main'

.products
    display: grid
    grid-template-columns: repeat(4, 1fr)
    justify-items: center
    @media (300px <= width <= 460px)
        grid-template-columns: repeat(1, 1fr)
    @media (460px <= width <= 810px)
        grid-template-columns: repeat(2, 1fr)

</style>