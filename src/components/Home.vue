<template>
  <div>
    <div id="home-jumbo">
      <h1>Lauren Namba</h1>
      <h4>Software Engineer</h4>
    </div>
    <About></About>
    <Projects></Projects>
    <Contact></Contact>
  </div>
</template>

<script>
import Vue from 'vue'
import About from './About.vue'
import Projects from './Projects.vue'
import Contact from './Contact.vue'

export default {
  data () {
    return {
    }
  },
  components: {
    'About': About,
    'Projects': Projects,
    'Contact': Contact,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
#home-jumbo {
  height: 100vh;
  background: linear-gradient(
      rgba(255, 61, 206, 0.35),
      rgba(255, 56, 164, 0.35)
    ), url('../assets/code.jpeg') no-repeat center center fixed;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
  background-size: cover;
  width: 100%;
  padding: 300px 0;
}

#home-jumbo h1 {
  font-size: 5em;
}

h1 {
  font-family: 'Oleo Script Swash Caps', 'Helvetica Neue', sans-serif;
}

h1, h2, h4 {
  font-weight: normal;
  color: #FFF;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
