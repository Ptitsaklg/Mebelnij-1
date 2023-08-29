<script setup>

const props = defineProps({
    img: {
        type: String,
        required: true,
    },
    title: {
        type: String,
        required: true,
    },
    price: {
        type: Number,
        required: true,
    },
})

</script>

<template>
    <div class="product">
        <routerLink to="/product">
            <img :src="img" :alt="title" class="image">
        </routerLink>
        <routerLink to="/product" class="title">{{ title }}</routerLink>
        <span class="price">{{ price }} &#8381;</span>
    </div> 
</template>

<style lang="sass" scoped>
@import '../assets/styles/main'

.image
    display: block
    margin-bottom: 10px

.title
    display: block
    margin-bottom: 10px
    max-width: 200px

.price
    display: block
    margin-bottom: 10px
    
</style>