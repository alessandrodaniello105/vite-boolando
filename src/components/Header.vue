<script>
export default {
  name: 'Header'

}
</script>

<template>
  <header>
     
    <!-- top-bar -->
    <div class="top-bar container d-flex">

      <!-- WEBSITE MENU -->
      <div class="menu website">
        <ul>
          <li><a href="#">Donna</a></li>
          <li><a href="#">Uomo</a></li>
          <li><a href="#">Bambini</a></li>
        </ul>
      </div>
      <!-- /WEBSITE MENU -->

      <!-- LOGO -->
      <div class="logo">
        <a href="#"><img src="assets/img/boolean-logo.png" alt="Logo Boolean"></a>
      </div>
      <!-- /LOGO -->
      
      <!-- USER MENU -->
      <div class="menu user">
        <a href="#"><i class="fa-regular fa-user"></i></a>
        <a href="#"><i class="fa-regular fa-heart"></i></a>
        <a href="#"><i class="fa-solid fa-bag-shopping"></i></a>
      </div>
      <!-- /USER MENU -->
      
    </div>
    <!-- top-bar -->

  </header>
</template>

<style>

</style>