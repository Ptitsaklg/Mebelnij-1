<script setup>

</script>

<template>
    <div class="interior-example">
        <div class="info">
            <div class="title">Для людей, кто любит неподвластный времени дизайн и качество</div>
            <routerLink to="/view-collection" class="view-collection">Просмотр коллекций</routerLink>
        </div>
    </div>
</template>

<style lang="sass" scoped>
@import '../assets/styles/main'

.interior-example
    background-image: url('/img/example.jpg')
    height: 650px
    background-size: 100%
    background-repeat: no-repeat
    margin: 30px 20px
    @media (810px <= width <= 1080px)
        height: 400px
    @media (300px <= width <= 530px)
        height: 270px
    @media (530px <= width <= 810px)
        height: 400px

.title
    font-weight: 500
    padding: 120px 50px 80px
    letter-spacing: 0.2em
    font-size: 22px
    @media (810px <= width <= 1080px)
        padding: 20px 50px 80px
    @media (300px <= width <= 345px)
        font-size: 16px
        padding: 160px 10px 30px
        text-align: center
    @media (345px <= width <= 500px)
        font-size: 16px
        padding: 250px 10px 30px
        text-align: center
    @media (500px <= width <= 810px)
        font-size: 16px
        padding: 20px 10px 30px
        text-align: center

.view-collection
    padding-left: 50px
    font-size: 25px
    font-weight: 500
    &:hover
        text-decoration: underline
    @media (300px <= width <= 810px)
        font-size: 17px
        font-weight: 600
        display: block
        text-align: center
        padding: 0
        padding-bottom: 30px
        
</style>