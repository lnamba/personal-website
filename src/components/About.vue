<template lang="html">
  <div id="about" class="col-md-12">
    <h1>Hi, I'm Lauren.</h1>
    <img src="../assets/headshot.jpg" alt="headshot">
    <h3>I am a teacher turned software engineer with a passion for designing and building amazing things. As an engineer, I am immersed in both creativity and problem solving, a rare but fun combination. I have a keen eye for design, and like to experiment with color, typography and functionality, but also enjoy solving logic challenges. Please check out some of my projects!</h3>
    <h1 id="skills">Skills</h1>
    <div class="row">
      <li class="col-md-6">
        <h5>JavaScript</h5>
        <b-progress v-model="js" :precision="1" show-progress variant="success"></b-progress>
      </li>
      <li class="col-md-6">
        <h5>HTML & CSS</h5>
        <b-progress v-model="html_css" :precision="1" show-progress variant="success"></b-progress>
      </li>
      <li class="col-md-6">
        <h5>jQuery</h5>
        <b-progress v-model="jquery" :precision="1" show-progress variant="success"></b-progress>
      </li>
      <li class="col-md-6">
        <h5>AJAX</h5>
        <b-progress v-model="ajax" :precision="1" show-progress variant="success"></b-progress>
      </li>
      <li class="col-md-6">
        <h5>AngularJS</h5>
        <b-progress v-model="angular" :precision="1" show-progress variant="success"></b-progress>
      </li>
      <li class="col-md-6">
        <h5>Vue.js</h5>
        <b-progress v-model="vue" :precision="1" show-progress variant="success"></b-progress>
      </li>
      <li class="col-md-6">
        <h5>Node.js (Express)</h5>
        <b-progress v-model="node_express" :precision="1" show-progress variant="success"></b-progress>
      </li>
      <li class="col-md-6">
        <h5>PostgreSQL</h5>
        <b-progress v-model="postgres" :precision="1" show-progress variant="success"></b-progress>
      </li>
    </div>
  </div>
</template>

<script>
export default {
  data(){
    return {
      js: 85,
      html_css: 90,
      jquery: 85,
      ajax: 85,
      angular: 75,
      vue: 75,
      node_express: 75,
      postgres: 75,
    }
  }
}
</script>

<style lang="css" scoped>

  h3 {
    line-height: 1.3;
  }

  #skills {
    margin: 50px 0;
  }

  #about {
    margin: 50px 0;
  }

  #about img {
    height: 300px;
    margin: 30px auto;
    border-radius: 50%;
    display: block;
  }

  li {
    list-style-type: none;
    margin-bottom: 10px;
  }

</style>
