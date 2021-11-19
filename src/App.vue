<template>
<div id="wrapper">
  
  <nav class="navbar is-dark">
    <div class="navbar-brand">
      <router-link to="/" class="navbar-item"><strong>Hoodie Shop</strong></router-link>
      <a class="navbar-burger" area-label="menu" aria-expanded="false" data-target = "navbar-menu">
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
        <span aria-hidden="true"></span>
      </a>
    </div>
    <div class="navbar-menu" id="navbar-menu">
      <div class = "navbar-end">
        <router-link to="/winter" class="navbar-item">Winter</router-link>
        <router-link to="/summer" class="navbar-item">Summer</router-link>
        <div class="navbar-item">
          <router-link to="/log-in" class="button is-success">Log In</router-link>
          <router-link to="/cart" class="button is-dark">
            <span class="icon">
              <i class="fas fa-shopping-cart"></i>
            </span>
            <span>Cart</span>
          </router-link>
        </div>
      </div>

    </div>
  </nav>
  
  <section class="section">
    <div class="container">
      <Home/>
      <router-view></router-view>
    </div>
  </section>
  <footer class="footer">
    <p class="has-text-centered">Copyright</p>

  </footer>
</div>
</template>

<script>
import Home from './views/Home';
export default {
  name: 'app',
  setup() {

  },
  components: {
    Home
  }
}
</script>

<style lang="scss">
@import '../node_modules/bulma';
</style>
