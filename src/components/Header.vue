<script setup>

const menu = [
    {
        name: 'Горшки для растений',
        path: '/pots'
    },
    {
        name: 'Керамика',
        path: '/ceramics'
    },
    {
        name: 'Столы',
        path: '/tables'
    },
    {
        name: 'Стулья',
        path: '/chairs'
    },
    {
        name: 'Посуда',
        path: '/crockery'
    },
    {
        name: 'Диваны',
        path: '/sofas'
    },
    {
        name: 'Декор',
        path: '/decor'
    },
]

</script>

<template>
    <header class="header">
        <div class="header-top">
            <img src="/svg/search.svg" alt="Search" class="search">
            <routerLink to="/" class="store-name">Мебельный №1</routerLink>
            <div class="right">
                <routerLink to="/basket"><img src="/svg/basket.svg" alt="basket" class="basket"></routerLink>
                <routerLink to="/user"><img src="/svg/user.svg" alt="user" class="user"></routerLink>
            </div>
        </div>
        <div class="line"></div>
        <div class="header-menu">
            <routerLink 
            to="/element.path" 
            class="menu-link"
            v-for="(element, key) of menu"
            :key="key"
            >
            {{ element.name }}
            </routerLink>
        </div>
    </header>
</template>

<style lang="sass" scoped>
@import '../assets/styles/main'

.header
    height: 160px
    padding: 40px 
    @media (300px <= width <= 810px)
        height: 250px
        padding: 20px

.header-top 
    display: grid
    grid-template-columns: repeat(3, 1fr)
    @media (300px <= width <= 810px)
        display: flex
        justify-content: space-between
 
    .search 
        width: 24px
        @media (300px <= width <= 810px)
            width: 18px

    .store-name
        font-size: 20px
        font-weight: 500
        @media (300px <= width <= 810px)
            font-size: 15px
            
    .right
        display: flex
        justify-content: flex-end

        .basket
            width: 30px
            margin-right: 16px
            @media (300px <= width <= 810px)
                width: 24px
                margin-right: 5px

        .user
            width: 30px
            @media (300px <= width <= 810px)
                width: 24px
            
.line
    margin: 10px 10px
    height: 1px
    background-color: #720dd6

.header-menu
    margin: 15px
    display: flex
    justify-content: center
    @media (300px <= width <= 810px)
       display: flex
       flex-direction: column
       
    .menu-link
        margin: 0 22px
        font-size: 18px
        &:hover
            text-decoration: underline
        @media (300px <= width <= 810px)
            display: flex
            justify-content: center
            font-size: 15px
            margin: 0 5px
            line-height: 1.8

</style>
