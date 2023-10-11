<script>
import { footerMenu, footerSocial } from '../data/menus';

export default {
  name: 'Footer',
  data() {
    return {
      footerMenu,
      footerSocial
    }
  }

}
</script>

<template>
  <footer>
    <div class="bottom-bar container d-flex justify-between">
      
      <nav class="box-informativa">

        <h2>Boolando s.r.l.</h2>

        <ul>
          <li v-for="(item, index) in footerMenu" :key="index"><a href="#">{{ item.text}}</a></li>
        </ul>

      </nav>
      
      <div class="box-social d-flex">

        <span>Trovaci anche su</span>

        <div class="social-icon">

          <ul>
            <li v-for="(item, index) in footerSocial" :key="index">
              <a href="#"><i class="fa-brands" :class="item.class"></i></a>
            </li>
          </ul>

        </div>

      </div>
      
    </div>

  </footer>
</template>

<style lang="scss" scoped>

footer {
  height: 100px;
  color: white;
  background-color: #1A1A1A;
  .bottom-bar {
    margin: 0 auto;
    padding-top: 25px;
    height: 100%;
    .box-informativa {
      h2 {
        margin-bottom: 10px;
      }
      ul li {
        position: relative;
        left: -5px;
        padding: 0 5px;
        display: inline-block;
        list-style: none;
      }
    }
    .box-social {
      font-weight: bold;
      flex-direction: column;
      align-items: center;
      .social-icon {
        padding-top: 10px;
        ul li {
          display: inline-block;
        }
        a {
          margin: 0 2px;
        }
      }
    }
    
  } 

}

</style>