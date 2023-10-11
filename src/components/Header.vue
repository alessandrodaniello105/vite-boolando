<script>
import { headerNav, headerMenu } from '../data/menus';

export default {

  name: 'Header',

  data() {
    return {
      headerNav,
      headerMenu
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
          <li v-for="(link, index) in headerNav" :key="index"><a href="#">{{ link.text }}</a></li>
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
        <ul>
          <li v-for="(item, index) in headerMenu" :key="index">
            <a href="#"><i :class="item.class"></i></a>
          </li>
        </ul>
      </div>
      <!-- /USER MENU -->
      
    </div>
    <!-- top-bar -->

  </header>
</template>

<style lang="scss" scoped>
header {
  position: fixed;
  top: 0;
  z-index: 999;
  height: 52px;
  width: 100vw;
  background-color: #FF6900;
  box-shadow: 0 0 3px 1px lighten(black, 40%);
  .top-bar {
    justify-content: space-between;
    align-items: center;
    margin: 0 auto;
    .menu {
      color: white;
      width: 25%;
      min-width: 190px;
      ul li {
        display: inline-block;
        list-style: none;
        padding-right: 5px;
      }
      &.user a i {
        padding-left: 10px;
        padding-bottom: 5px;
      }
    }
    
  }
}


</style>