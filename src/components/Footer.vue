<script>
export default {
  name: 'Footer'

}
</script>

<template>
  <footer>
    <div class="bottom-bar container d-flex justify-between">
      
      <nav class="box-informativa">
        <h2>Boolando s.r.l.</h2>
        <ul>
          <li><a href="#">Informazioni legali</a></li>
          <li><a href="#">Informativa sulla privacy</a></li>
          <li><a href="#">Diritto di recesso</a></li>
        </ul>
      </nav>
      
      <div class="box-social d-flex">
        <span>Trovaci anche su</span>
        <div class="social-icon">
          <a href="#"><i class="fa-brands fa-square-twitter"></i></a>
          <a href="#"><i class="fa-brands fa-square-facebook"></i></a>
          <a href="#"><i class="fa-brands fa-square-instagram"></i></a>
          <a href="#"><i class="fa-brands fa-square-pinterest"></i></a>
          <a href="#"><i class="fa-brands fa-square-youtube"></i></a>
        </div>
      </div>
      
    </div>

  </footer>
</template>

<style lang="scss" scoped>
@use '../scss/partials/_utilities.scss' as *;

footer {
  height: 100px;
  color: white;
  background-color: #1A1A1A;
}

footer h2 {
  font-size: 1.2rem;
}

footer ul {
  font-size: 0.8rem;
}

footer ul li {
  position: relative;
  left: -5px;
  padding: 0 5px;
}

.bottom-bar .box-informativa ul li {
  display: inline-block;
  list-style: none;
}

.bottom-bar {
  margin: 0 auto;
  padding-top: 25px;
  height: 100%;
} 

.box-informativa h2 {
  margin-bottom: 10px;
}

.box-social {
  font-weight: bold;
  flex-direction: column;
  align-items: center;
}

.box-social span {
  font-size: 0.8rem;
}

.box-social .social-icon {
  padding-top: 10px;
  font-size: 1.5rem;
}

.box-social .social-icon a {
  color: white;
}
</style>