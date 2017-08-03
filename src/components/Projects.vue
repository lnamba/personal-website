<template>
  <div id="projects">
    <h1 id="project_h1">Projects</h1>
    <b-card class="mb-2" v-for="project in projects" :key="project.id" :id="'q'+project.id">
      <h1>{{ project.title }}</h1>
      <img :src="project.img_url" :alt="project.title" class="col-md-10">
      <h2 :style="{marginTop:20+'px'}">{{ project.description }}</h2>
      <div class="demo">
        <a :href="project.link" :style="{marginBottom:10+'px'}">VIEW DEMO</a>
      </div>
      <div class="github">
        <h4>Github</h4>
        <a :href="project.github_url"><img src="../assets/GitHub-black.png" alt="GitHub"></a>
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
      projects: [
        {
          id: 1,
          title: '7 Jumbled Words',
          img_url: require('../assets/q1.png'),
          description: 'An addictive vocabulary puzzle for word nerds',
          link: 'https://g47-q1-project.herokuapp.com/',
          github_url: 'https://github.com/lnamba/Quarter1_Project_WordGame'
        },
        {
          id: 2,
          title: `Let's Eat!`,
          img_url: require('../assets/q2.png'),
          description: 'A CRUD app allowing family members to suggest dinner for the night',
          link: 'https://g47-group-project.herokuapp.com/',
          github_url: 'https://github.com/lnamba/Q2-My-Version'
        },
        {
          id: 3,
          title: 'ThinkPlan',
          img_url: require('../assets/q3.png'),
          description: 'A simple and clean lesson planning app for teachers',
          github_url: 'https://github.com/lnamba/thinkplan'
        },
        {
          id: 4,
          title: 'Hanyu.co',
          img_url: require('../assets/q4.png'),
          description: 'A Mandarin Chinese educational app that gamifies the language learning experience (collaboration with Spiffy Ventures)',
          link: 'https://g47-capstone.herokuapp.com/',
          github_url: 'https://github.com/lnamba/g47-Capstone-Project'
        }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

#project_h1 {
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
  margin: 50px 0;
}

.github img {
  height: 50px;
}

</style>
