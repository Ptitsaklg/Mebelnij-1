<script setup>

const aboutBrands = [
    {
        img: '/img/about-brand-1.png',
        title: 'Ежедневное высокое качество работы',
        description: 'Какое-то описание особенностей работы'
    },
    {
        img: '/img/about-brand-2.png',
        title: 'Сделано настоящими мастерами',
        description: 'Какое-то описание особенностей работы'
    },
    {
        img: '/img/about-brand-3.png',
        title: 'Оптимальное соотношение цена/качество',
        description: 'Какое-то описание особенностей работы'
    },
    {
        img: '/img/about-brand-4.png',
        title: 'Только экологически чистые материалы',
        description: 'Какое-то описание особенностей работы'
    },
]
</script>

<template>
    <div class="title">Что отличает наш бренд от других</div>
    <div class="elements">
        <div 
            class="element"
            v-for="(element, key) of aboutBrands"
            :key="key"
            >
            <img 
            class="element-img"
            :src="element.img"
            :alt="element.title"
            />
            <div class="element-title">{{ element.title }}</div>
            <span class="element-description">{{ element.description }}</span>
        </div>
    </div>
</template>

<style lang="sass" scoped>
@import '../assets/styles/main'

.title
    display: flex
    justify-content: center
    text-align: center
    margin: 120px 10px 15px
    @media (530px <= width <= 810px)
        margin: 10px 10px 10px   

.elements
    display: grid
    grid-template-columns: repeat(4, 240px)
    justify-content: space-between
    justify-items: center
    margin-bottom: 50px
    @media (810px <= width <= 1080px)
        grid-template-columns: repeat(2, 1fr)
        gap: 40px 20px
    @media (300px <= width <= 810px)
        grid-template-columns: repeat(1, 1fr)
        margin-bottom: 20px

.element
    margin: 0 10px 30px
    @media (300px <= width <= 810px)
       display: block
       text-align: center

.element-title
    font-weight: 600
    padding-bottom: 10px
    
</style>

