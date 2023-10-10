<script>

import productCards from '../data/productCards'

export default {
  name: 'Main',
  data() {
    return {
      productCards
    }
  }

}
</script>

<template>
  <main>
  
    <!-- MAIN WRAPPER -->
    <div class="main-wrap d-flex container justify-between">

      <!-- PRODOTTO 1 -->
      <div v-for="(product, index) in productCards" :key="index" class="product">
        
        <!-- IMAGE BOX -->
        <div class="big-col">
          
          <div class="img-product">
            <img :src="product.urlA" alt="">
            <img :src="product.urlB" alt="">
          </div>
          
          <span class="heart">&hearts;</span>
          
          <div class="img-bottom-text">
            <span class="badge discount-percent">-50%</span>
            <span class="badge green-choice">Sostenibilità</span>
          </div>
        
        </div>
        <!-- /IMAGE BOX -->
        
        <!-- TEXT BOX -->
        <div class="small-col">
          <div class="text-box">
            
            <span class="product-brand">Levi's</span>
            
            <h2 class="product-model">Relaxed fit tee unisex</h2>
            
            <span class="discount price">14,99 € </span>
            
            <span class="original price">29,99 €</span>
            
          </div>      
        </div>
        <!-- /TEXT BOX -->
        
      </div>
      <!-- /PRODOTTO 1 -->
      
    </div>
    <!-- /MAIN WRAPPER -->

  </main>
</template>

<style>

</style>