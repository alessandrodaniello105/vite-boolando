<script>

import ProductCard from './ProductCard.vue';

export default {
  name: 'Main',
  components: {
    ProductCard
  }

}
</script>

<template>
  <main>
  
    <!-- MAIN WRAPPER -->
    <div class="main-wrap d-flex container justify-between">

      <ProductCard />
      
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