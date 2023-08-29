<script setup>
import Header from '../components/Header.vue';
import InteriorExample from '../components/InteriorExample.vue';
import BrandFeature from '../components/BrandFeature.vue';
import ProductExamples from '../components/ProductExamples.vue';
import Subscribe from '../components/Subscribe.vue';

</script>

<template>
    <div class="container">
        <Header></Header>
        <InteriorExample></InteriorExample>
        <BrandFeature></BrandFeature>
        <ProductExamples></ProductExamples>
        <Subscribe></Subscribe>
    </div>
</template>

<style lang="sass" scoped>
@import '../assets/styles/main'

.container
    max-width: 1440px
    margin: auto
    
</style>
