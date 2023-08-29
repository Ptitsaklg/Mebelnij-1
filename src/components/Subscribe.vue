<script setup>

</script>

<template>
    <div class="subscribe">
        <div class="content">
            <h3 class="title">Присоединяйтесь к клубу и получайте преимущества</h3>
            <div class="description">Подписывайтесь на нашу рассылку и получайте эксклюзивные предложения по новому ассортименту, распродаже и многому другому</div>
        </div>
        <div class="checks">
            <div class="check">
                <img src="/svg/check.svg" alt="check-img" class="check-img">
                <span class="check-name">Эксклюзивные предложения</span>
            </div>
            <div class="check">
                <img src="/svg/check.svg" alt="check-img" class="check-img">
                <span class="check-name">Бесплатные мероприятия</span>
            </div>
            <div class="check">
                <img src="/svg/check.svg" alt="check-img" class="check-img">
                <span class="check-name">Скидки</span>
            </div>
        </div>
        <form class="form">
            <input type="text" placeholder="Email" class="input-text">
            <button type="subscribe" class="input-btn">Подписаться</button>
        </form>
    </div>
</template>

<style lang="sass" scoped>
@import '../assets/styles/main'

.subscribe
    background: url('/img/subscribe.jpg')
    height: 750px
    background-size: 100%
    background-repeat: no-repeat
    margin: 30px 10px
    @media (300px <= width <= 810px)
        height: 350px
        
.content
    max-width: 600px
    text-align: center
    margin: auto

    .title
        padding-top: 100px
        @media (300px <= width <= 810px)
            padding-top: 10px
            font-size: 15px

    .description
        font-size: 15px
        @media (300px <= width <= 810px)
            font-size: 12px
            padding-bottom: 40px

.checks
    display: flex
    justify-content: center
    padding-top: 50px
    @media (300px <= width <= 390px)
        flex-direction: column
        padding-top: 70px
    @media (390px <= width <= 490px)
        flex-direction: column
        padding: 0 0 60px 10px
    @media (490px <= width <= 810px)
        flex-direction: column
        padding: 0 0 0 10px

.check
    display: flex
    align-items: center
    @media (300px <= width <= 810px)       

    .check-img
        width: 14px
        margin-right: 5px

    .check-name
        font-size: 14px
        margin-right: 40px
        @media (300px <= width <= 810px)
            margin: 0
        
.form
    display: flex
    justify-content: center
    padding-top: 60px
    @media (300px <= width <= 490px)
        padding-top: 20px
        padding-bottom: 40px
    @media (490px <= width <= 810px)
        padding-top: 20px

    .input-text
        padding: 16px
        width: 300px
        font-size: 15px
        @media (300px <= width <= 810px)
            padding: 7px
            width: 150px

    .input-btn
        width: 130px
        background-color: #1e277d
        color: white
        font-size: 15px
        &:hover
            background-color: darken(#1e277d, 12%)
        @media (300px <= width <= 810px)
            width: 105px
            
</style>