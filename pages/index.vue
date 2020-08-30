<template>
  <div>
    <product-slides/>
    <section-cards/>
    
  </div>
</template>
<script>
import ProductSlides from '@/components/product/ProductSlides.vue';
import SectionCards from '@/components/product/SectionCards.vue';

export default {
components:{
  ProductSlides,
  SectionCards
},
  head :{
    title:'Amsterdam Apothecary Home'
  }
}
</script>

<style>

</style>
