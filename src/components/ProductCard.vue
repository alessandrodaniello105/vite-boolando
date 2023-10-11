<script>
export default {
name: 'ProductCard',

props: {
  product: Object
},

computed: {
  formattedPrice() {
    return `${this.product.price} &euro;`
  },

  formattedPriceNew() {
    return `${this.product.priceNew} &euro; &MediumSpace;`
  }
},

created() {
  console.log(this.formattedPrice)
}

}
</script>

<template>
  <div class="product">

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
          <span class="discount price" v-html="formattedPriceNew"></span>
        
          <span class="original price" v-html="formattedPrice"> </span>
        </div>
        <span v-else class="discount price" v-html="formattedPrice"> </span>

        
      </div>      
    </div>
    <!-- /TEXT BOX -->
    
  </div>
</template>

<style lang="scss" scoped>

.product {
  width: 33%;
  max-width: 390px;
  min-width: 245px;
  margin: 20px 0;
  /* BIG COL (IMAGE BOX) */
  .big-col {
    position: relative;
    cursor: pointer;
    img {
      width: 100%;
    }
    img:last-child {
      display: none;
      position: absolute;
      top: 0;
      left: 0;
    }
    &:hover img:last-child {
      display: block;
    }

    .heart {
      position: absolute;
      top: 20px; 
      right: 0;
      background-color: white;
      font-size: 2rem;
      padding: 5px 15px;
      &:hover {
        color: red;
      }
      &.fav {
        color: red;
      }
    }

    .img-bottom-text {
      position: absolute;
      bottom: 40px;
      font-size: 0.8rem;
      font-weight: bold;
      color: white;

      .badge {
        padding: 5px 10px;
      }
      .discount-percent {
        background-color: red;
      }
      .green-choice {
        background-color: green;
      }
    }
  

  }

  .big-col,
  .small-col {
    width: 100%;
  }


}

</style>