<script>
import productCards from '../data/productCards'

export default {
name: 'ProductCard',
data(){
  return {
    productCards
  }
}
}
</script>

<template>
  <div v-for="(product, index) in productCards" :key="index" class="product">

    <!-- IMAGE BOX -->
    <div class="big-col">
            
      <div class="img-product">
        <img :src="product.urlA" alt="">
        <img :src="product.urlB" alt="">
      </div>
      
      <span @click="product.isFav = !product.isFav" :class="{'fav': product.isFav}" class="heart">&hearts;</span>
      
      <div class="img-bottom-text">
        <span v-if="product.isDiscounted" class="badge discount-percent">-{{product.discountPercentage}}&percnt;</span>
        <span v-if="product.isEco" class="badge green-choice">Sostenibilità</span>
      </div>
    
    </div>
    <!-- /IMAGE BOX -->
    
    <!-- TEXT BOX -->
    <div class="small-col">
      <div class="text-box">
        
        <span class="product-brand">{{ product.productInfo.brand }}</span>
        
        <h2 class="product-model">{{ product.productInfo.model }}</h2>
        
        <div v-if="product.isDiscounted" >
          <span class="discount price">{{ product.priceNew }} € </span>
        
          <span class="original price">{{ product.price }}€</span>
        </div>
        <span v-else class="discount price">{{ product.price }}€</span>

        
      </div>      
    </div>
    <!-- /TEXT BOX -->
    
  </div>
</template>

<style>
.product {
  width: 33%;
  max-width: 390px;
  min-width: 245px;
  margin: 20px 0;
}

.product .big-col,
.product .small-col {
  width: 100%;
}

/* BIG COL (IMAGE BOX) */

.big-col {
  cursor: pointer;
}

.big-col img:last-child {
  display: none;
  position: absolute;
  top: 0;
  left: 0;
}

.big-col:hover img:last-child {
  display: block;
}

.product .big-col {
  position: relative;
}

.product img {
  width: 100%;
}

.product .heart {
  position: absolute;
  top: 20px; 
  right: 0;
  background-color: white;
  padding: 5px 15px;
  font-size: 2rem;
}

.product .heart:hover {
  color: red;
}

.product .heart.fav {
  color: red;
}

.img-bottom-text {
  position: absolute;
  bottom: 40px;
  font-size: 0.8rem;
  font-weight: bold;
  color: white;
}

.img-bottom-text .badge {
  padding: 5px 10px;
}

.img-bottom-text .discount-percent {
  background-color: red;
}

.img-bottom-text .green-choice {
  background-color: green;
}

/* SMALL COL (TEXT BOX) */

.text-box span:first-child {
  font-size: 0.9rem;
}

.text-box h2 {
  text-transform: uppercase;
  font-size: 1rem;
}

.product-brand,
.discount.price,
.original.price {
  font-size: 0.9rem;
}

.discount.price {
  color: red;
  font-weight: bold;
}

.original.price {
  text-decoration: underline;
  text-underline-offset: -40%;
  text-decoration-skip-ink: none;
}
</style>