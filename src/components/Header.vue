<script>
export default {
  name: 'Header',
  data() {
    return {
      mainMenu: [
        'Donna',
        'Uomo',
        'Bambini'
      ]
    }
  }

}
</script>

<template>
  <header>
     
    <!-- top-bar -->
    <div class="top-bar container d-flex h-100">

      <!-- WEBSITE MENU -->
      <nav class="menu website">
        <ul>
          <li v-for="(link, index) in mainMenu" :key="index"><a href="#">{{ link }}</a></li>
        </ul>
      </nav>
      <!-- /WEBSITE MENU -->

      <!-- LOGO -->
      <div class="logo w-50">
        <a href="#"><img src="/boolean-logo.png" class="ht-25" alt="Logo Boolean"></a>
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

<style scoped>
header {
  position: fixed;
  top: 0;
  z-index: 999;
  height: 50px;
  width: 100vw;
  background-color: #FF6900;
  box-shadow: 0 0 2px  black;
}

.top-bar {
  justify-content: space-between;
  align-items: center;
  margin: 0 auto;
}

.top-bar ul li {
  padding-right: 5px;
}

.top-bar ul li {
  display: inline-block;
  list-style: none;
}

.top-bar .menu {
  color: white;
  width: 25%;
  min-width: 190px;
}



.top-bar .menu.user a i {
  padding-left: 5px;
  padding-bottom: 5px;
}
</style>