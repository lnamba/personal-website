<template lang="html">
  <div id="about" class="col-md-12">
    <h1>Hi, I'm Lauren.</h1>
    <img src="../assets/headshot.jpg" alt="headshot">
    <h3>I am a teacher turned software engineer with a passion for designing and building amazing things. As an engineer, I am immersed in both creativity and problem solving, a rare but fun combination. I have a keen eye for design, and like to experiment with color, typography and functionality, but also enjoy solving logic challenges. Please check out some of my projects!</h3>
    <h1 id="skills">Skills</h1>
    <div class="row">
      <div class="col-md-3 skill" v-for="skill in skills" :key="skill.id">
        <label :for="skill.nickname">{{ skill.name }}</label>
        <div :id="skill.nickname" @mouseenter.once.self="showSkill(skill)"></div>
      </div>
    </div>
      <!-- <li class="col-md-6">
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
      </li> -->
    </div>
  </div>
</template>

<script>
const d3 = require("d3");
import jQuery from 'jQuery'
window.jQuery = jQuery

export default {
  data(){
    return {
      skills: [
        {
          id: 1,
          name: 'JavaScript',
          nickname: 'js',
          level: 85,
        },
        {
          id: 2,
          name: 'HTML/CSS',
          nickname: 'html_css',
          level: 90,
        },
        {
          id: 3,
          name: 'jQuery',
          nickname: 'jquery',
          level: 85,
        },
        {
          id: 4,
          name: 'AJAX',
          nickname: 'ajax',
          level: 85,
        },
        {
          id: 5,
          name: 'AngularJS',
          nickname: 'angular',
          level: 80,
        },
        {
          id: 6,
          name: 'Vue',
          nickname: 'vue',
          level: 80,
        },
        {
          id: 7,
          name: 'Node.js (Express)',
          nickname: 'node_express',
          level: 80,
        },
        {
          id: 8,
          name: 'PostgreSQL',
          nickname: 'postgres',
          level: 75,
        },
      ],
    }
  },
  mounted(){
    this.showAllSkills()
  },
  methods: {
    drawDonutChart(element, percent, width, height, text_y) {
        let duration = 1500, transition = 200;
        let colors = ['#09BD1D', '#000']
        width = typeof width !== 'undefined' ? width : 200;
        height = typeof height !== 'undefined' ? height : 200;
        text_y = typeof text_y !== 'undefined' ? text_y : "-.10em";

        let dataset = {
          lower: calcPercent(0),
          upper: calcPercent(percent)
        },
        radius = Math.min(width, height) / 2,
        pie = d3.pie().sort(null),
        format = d3.format(".0%");

        var arc = d3.arc()
        .innerRadius(radius - 30)
        .outerRadius(radius);

        var svg = d3.select(element).append("svg")
        .attr("width", width)
        .attr("height", height)
        .append("g")
        .attr("transform", "translate(" + width / 2 + "," + height / 2 + ")");

        var path = svg.selectAll("path")
        .data(pie(dataset.lower))
        .enter().append("path")
        .style("fill", function(d, i) { return colors[i] })
        .attr("class", function(d, i) { return "color" + i })
        .attr("d", arc)
        .each(function(d,i) { this._current = d; });

        var text = svg.append("text")
        .attr("text-anchor", "middle")
        .attr("dy", text_y)
        .style("font-size", "2em")
        .style("color", "#FFF")
        .style("font-family", "'Oleo Script Swash Caps', 'Helvetica Neue', sans-serif")

        if (typeof(percent) === "string") {
          text.text(percent);
        }
        else {
          var progress = 0;
          var timeout = setTimeout(function () {
            clearTimeout(timeout);
            path = path.data(pie(dataset.upper)); // update the data
            path.transition().duration(duration).attrTween("d", function (a) {
              var i  = d3.interpolate(this._current, a);
              var i2 = d3.interpolate(progress, percent)
              this._current = i(0);
              return function(t) {
                text.text( format(i2(t) / 100) );
                return arc(i(t));
              };
            });
          }, 200);
        }

        function calcPercent(percent) {
          return [percent, 100-percent];
        };
    },
    showAllSkills(){

      for (let i = 0; i < this.skills.length; i++) {
        console.log(`${this.skills[i].nickname}`);
        this.drawDonutChart(`#${this.skills[i].nickname}`, (this.skills[i].level/100).toFixed(2) * 100, 200, 200, '.35em');

        // drawDonutChart('#js', (this.js/100).toFixed(2) * 100, 200, 200, '.35em');
        // drawDonutChart('#html_css', (this.html_css/100).toFixed(2) * 100, 200, 200, '.35em');
        // drawDonutChart('#jquery', (this.jquery/100).toFixed(2) * 100, 200, 200, '.35em');
        // drawDonutChart('#ajax', (this.ajax/100).toFixed(2) * 100, 200, 200, '.35em');
        // drawDonutChart('#angular', (this.angular/100).toFixed(2) * 100, 200, 200, '.35em');
        // drawDonutChart('#vue', (this.vue/100).toFixed(2) * 100, 200, 200, '.35em');
        // drawDonutChart('#node_express', (this.node_express/100).toFixed(2) * 100, 200, 200, '.35em');
        // drawDonutChart('#postgres', (this.postgres/100).toFixed(2) * 100, 200, 200, '.35em');
      }
    },
    showSkill(skill) {
      jQuery(`#${skill.nickname}`).empty()
      this.drawDonutChart(`#${skill.nickname}`, (skill.level/100).toFixed(2) * 100, 200, 200, '.35em')
    },
    prevented(skill){
      !this.showSkill(skill)
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

  label {
    font-family: 'Metrophobic', Helvetica, Arial, sans-serif;
    /*font-family: 'Muli', sans-serif;
    font-family: 'Nunito', sans-serif;*/
    font-size: 1.5em;
  }

  .skill {
    margin-bottom: 50px
  }

</style>
