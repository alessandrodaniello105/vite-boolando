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
        <a href="#"><img src="/boolean-logo.png" alt="Logo Boolean"></a>
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
  width: 100%;
  background-color: #FF6900;
  box-shadow: 0 0 2px  black;
}

.top-bar {
  justify-content: space-between;
  align-items: center;
  margin: 0 auto;
  height: 100%;
}

.top-bar ul li {
  padding-right: 5px;
  font-weight: bold;
  font-size: 0.9rem;
}

.top-bar ul li,
.bottom-bar .box-informativa ul li {
  display: inline-block;
  list-style: none;
}



.top-bar a:hover {
  text-underline-offset: 5px;
  text-decoration-thickness: 0rem;
}

.top-bar .menu {
  color: white;
  width: 25%;
  min-width: 190px;
}

.top-bar .menu.user {
  text-align: right;
}

.top-bar .menu.user a i {
  text-align: right;
  font-size: 0.7rem;
  padding-left: 5px;
  padding-bottom: 5px;
}

.top-bar .logo {
  text-align: center;
  width: 50%;
}

.top-bar img {
  height: 25px;
}

</style>