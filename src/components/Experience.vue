<template lang="html">
  <div id="experience">
    <h1>Experience</h1>
    <div class="row">
      <b-card class="mb-2 col-md-8" id="role1">
        <h2><b>Software Engineer I</b></h2>
        <div>
          <h4>Infusionsoft / Chandler, AZ / August 2017 - Present</h4>
          <!-- <h4>Infusionsoft</h4>
          <h4>Chandler, AZ</h4>
          <h4>August 2017 - Present</h4> -->
        </div>
      </b-card>
    </div>
    <div class="row">
      <b-card class="mb-2 col-md-8" id="role2">
        <h2><b>Web Development Teaching Assistant</b></h2>
        <div>
          <h4>Galvanize / Phoenix, AZ / March 2017 - May 2017</h4>
          <!-- <h4>Galvanize</h4>
          <h4>Phoenix, AZ</h4>
          <h4>March 2017 - May 2017</h4> -->
        </div>
      </b-card>
    </div>
    <div class="row">
      <b-card class="mb-2 col-md-8" id="role3">
        <h2><b>Assistant Language Teacher of English</b></h2>
        <div>
          <h4>Phoenix Sister Cities Teach Abroad Program / Himeji, Japan / January 2014 - December 2015</h4>
          <!-- <h4>Phoenix Sister Cities Teach Abroad Program</h4>
          <h4>Himeji, Japan</h4>
          <h4>January 2014 - December 2015</h4> -->
        </div>
      </b-card>
    </div>
    <div class="row">
      <b-card class="mb-2 col-md-8" id="role4">
        <h2><b>Teacher</b></h2>
        <div>
          <h4>Peoria Unified School District / Peoria, AZ / December 2010 - May 2013</h4>
          <!-- <h4>Peoria Unified School District</h4>
          <h4>Peoria, AZ</h4>
          <h4>December 2010 - May 2013</h4> -->
        </div>
      </b-card>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      role: []
    }
  }
}
</script>

<style lang="css" scoped>

  #experience {
    margin: 50px 0;
  }

  .role h3 {
    /*font-size: 1.7em;*/
    font-family: 'Metrophobic', Helvetica, Arial, sans-serif;
    /*font-family: 'Muli', sans-serif;
    font-family: 'Nunito', sans-serif;*/
  }

  .row {
    height: 142px;
    /*margin: 0 auto;*/
  }

  .mb-2 {
    margin: 0 auto;
  }

</style>
