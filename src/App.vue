<template>
  <div id="app">
    <b-navbar toggleable type="inverse" variant="inverse" sticky>

      <b-nav-toggle target="nav_collapse"></b-nav-toggle>

      <b-link class="navbar-brand" to="#">
        <img id="brand" src="./assets/logo2.svg" alt="brand">
      </b-link>

      <b-collapse is-nav id="nav_collapse">
        <b-nav is-nav-bar>
          <b-nav-item id="name"><router-link :to="{ name: 'Home', params: {} }">Lauren Namba</router-link></b-nav-item>
        </b-nav>
        <b-nav is-nav-bar class="ml-auto">
          <b-nav-item-dropdown text="Take me to..." right>
            <b-dropdown-item href="#about">About</b-dropdown-item>
            <b-dropdown-divider></b-dropdown-divider>
            <b-dropdown-item href="#projects" >Projects</b-dropdown-item>
            <b-dropdown-divider></b-dropdown-divider>
            <b-dropdown-item href="#experience">Experience & Education</b-dropdown-item>
          </b-nav-item-dropdown>
        </b-nav>

      </b-collapse>
    </b-navbar>

    <!-- BODY -->
    <router-view></router-view>
  </div>
</template>

<script>
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'
export default {
  name: 'app'
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Oleo+Script+Swash+Caps|Metrophobic|Muli|Nunito');

  #app {
    font-family: 'Metrophobic', Helvetica, Arial, sans-serif;
    /*font-family: 'Muli', sans-serif;
    font-family: 'Nunito', sans-serif;*/
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
  }

  #brand {
    height: 50px;
  }

  #name {
    font-family: 'Oleo Script Swash Caps', Helvetica, Arial, sans-serif;
  }

  h1 {
    font-family: 'Oleo Script Swash Caps', Helvetica, Arial, sans-serif;
    font-size: 5em;
  }

  #heading {
    font-size: 5em;
  }

  .nav-item a, .link {
    color: #FFF;
    font-size: 1.2em;
  }

  .nav-item a:hover, .nav-item a:active,
  .link:hover, .link:active {
    color: #AAA;
    text-decoration: none;
  }

  .nav-item a:focus, .link:focus {
    color: #FFF;
    text-decoration: none;
  }

  .dropdown-menu a {
    color: #000;
  }

  .dropdown-menu a:hover {
    color: #FFF;
  }

</style>
