<script>

import ProductCard from './ProductCard.vue';
import products from '../data/productCards'

export default {
  name: 'Main',
  components: {
    ProductCard
  },
  data() {
    return {
      products
    }
  }

}
</script>

<template>
  <main>
  
    <!-- MAIN WRAPPER -->
    <div class="main-wrap d-flex container justify-between">

      <ProductCard
        v-for="product in products"
        :key="product.id"
        :product="product"
      />
      
    </div>
    <!-- /MAIN WRAPPER -->

  </main>
</template>

<style scoped>

.main-wrap {
  flex-wrap: wrap;
  padding-top: 60px;
  margin: 40px auto;
  width: 98%;
}

</style>