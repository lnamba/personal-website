<template>
  <div>
    <h1 id="projects">Projects</h1>
    <b-card class="mb-2" id="q1">
      <h1>7 Jumbled Words</h1>
      <img src="../assets/q1.png" alt="7 Jumbled Words" class="col-md-12">
      <h2 :style="{marginTop:20+'px'}">An addictive vocabulary puzzle for word nerds</h2>
      <div class="demo">
        <a href="https://g47-q1-project.herokuapp.com/" :style="{marginBottom:10+'px'}">VIEW DEMO</a>
      </div>
      <div class="github">
        <h4>Github</h4>
        <a href="https://github.com/lnamba/Quarter1_Project_WordGame"><img src="../assets/GitHub-black.png" alt="GitHub"></a>
      </div>
    </b-card>

    <b-card class="mb-2" id="q2">
      <h1>Let's Eat!</h1>
      <img src="../assets/q2.png" alt="Let's Eat!" class="col-md-12">
      <h2 :style="{marginTop:20+'px'}">A CRUD app allowing family members to suggest dinner for the night</h2>
      <div class="demo">
        <a href="https://g47-group-project.herokuapp.com/" :style="{marginBottom:10+'px'}">VIEW DEMO</a>
      </div>
      <div class="github">
        <h4>Github</h4>
        <a href="https://github.com/lnamba/Q2-My-Version"><img src="../assets/GitHub-black.png" alt="GitHub"></a>
      </div>
   </b-card>

   <b-card class="mb-2" id="q3">
     <h1>ThinkPlan</h1>
     <img src="../assets/q3.png" alt="ThinkPlan" class="col-md-12">
     <h2 :style="{margin:20+'px ' + 0}">A simple and clean lesson planning app for teachers</h2>
    <!-- <div class="demo">
      <a href="https://g47-q1-project.herokuapp.com/" :style="{marginBottom:10+'px'}">VIEW DEMO</a>
    </div> -->
     <div class="github">
       <h4>Github</h4>
       <a href="https://github.com/lnamba/thinkplan"><img src="../assets/GitHub-black.png" alt="GitHub"></a>
     </div>
   </b-card>

   <b-card class="mb-2" id="q4">
     <h1>Hanyu.co</h1>
     <img src="../assets/q4.png" alt="Hanyu.co" class="col-md-12">
     <h2 :style="{marginTop:20+'px'}">A Mandarin Chinese educational app that gamifies the language learning experience (collaboration with Spiffy Ventures)</h2>
     <div class="demo">
       <a href="https://g47-capstone.herokuapp.com/" :style="{marginBottom:10+'px'}">VIEW DEMO</a>
     </div>
     <div class="github">
       <h4>Github</h4>
       <a href="https://github.com/lnamba/g47-Capstone-Project"><img src="../assets/GitHub-black.png" alt="GitHub"></a>
     </div>
  </b-card>
  </div>
</template>

<script>
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'
export default {
  data () {
    return {
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
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

#projects {
  background: linear-gradient(
      rgba(85, 25, 181, 1),
      rgba(91, 192, 222, 1)
    );
  /*background-color: #5519B5;*/
  margin: 0;
  padding: 50px 0;
  color: #FFF;
  font-size: 5em;
}

h1 {
  font-size: 4em;
  font-family: 'Oleo Script Swash Caps', 'Helvetica Neue', sans-serif;
  margin: 50px 0;
}

#q1 {
  /*border top is allowing card and projects h1 to combine seamlessly*/
  border-top: none;
  background-color: #5BC0DE;
}

#q1 h1,
#q1 .demo a {
  color: #FFF;
}

#q2 {
  /*background-color: #D55B27;*/
  background-color: #E4538D;
}

#q2 h1,
#q2 .demo a {
  color: #FFF;
}

#q3 {
  background-color: #EBC335;
}

#q3 h1 {
  color: #FFF;
}

#q4 {
  background-color: #E83232;
}

#q4 h1 {
  color: #FFF;
}

#q4 h1,
/*#q4 h2,*/
#q4 .demo a {
  color: #FFF;
}

.card-block, .demo, .github {
  font-size: 1.1em;
}

.demo {
  margin-top: 20px;
}

.github {
  margin: 50px 0 10px 0;
}

.github img {
  height: 50px;
}

</style>
