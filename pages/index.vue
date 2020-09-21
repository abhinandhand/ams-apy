<template>
  <div>
    <product-slides/>
    <section-cards/>
    <about/>
    <features/>
    <benefits/>
    <!-- <gallery/> -->
    
  </div>
</template>
<script>
import ProductSlides from '@/components/product/ProductSlides.vue';
import SectionCards from '@/components/product/SectionCards.vue';
import About from '@/components/product/About.vue';
import Features from '@/components/product/Features.vue';
import Benefits from '@/components/product/Benefits.vue';
import Gallery from '@/components/product/Gallery.vue';

export default {
components:{
  ProductSlides,
  SectionCards,
  About
},
  head :{
    title:'Amsterdam Apothecary Home'
  }
}
</script>

<style>

</style>
