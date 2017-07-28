<template lang="html">
  <div>
    <div id="experience">
      <h1>Experience</h1>
      <div class="row" v-for="role in roles">
        <b-card class="mb-2 col-md-8">
          <h2><b>{{ role.title }}</b></h2>
          <div>
            <h4>{{ role.company }}</h4>
            <h4>{{ role.location }}</h4>
            <h4>{{ role.dates }}</h4>
          </div>
        </b-card>
      </div>
    </div>
    <div id="education">
      <h1>Education</h1>
      <div class="row" v-for="ed in education">
        <b-card class="mb-2 col-md-8">
          <h2><b>{{ ed.program }}</b></h2>
          <div>
            <h4>{{ ed.school }}</h4>
            <h4>{{ ed.location }}</h4>
            <h4>{{ ed.date }}</h4>
            <h4 v-if="ed.honors">{{ ed.honors }}</h4>
          </div>
        </b-card>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      roles: [
        {
          title: 'Software Engineer I',
          company: 'Infusionsoft',
          location: 'Chandler, AZ',
          dates: 'August 2017 - Present'
        },
        {
          title: 'Web Development Teaching Assistant',
          company: 'Galvanize',
          location: 'Phoenix, AZ',
          dates: 'March 2017 - May 2017'
        },
        {
          title: 'Customer Service Representative',
          company: 'General Dynamics Information Technology',
          location: 'Phoenix, AZ',
          dates: 'August 2016 - January 2017'
        },
        {
          title: 'Assistant Language Teacher of English',
          company: 'Phoenix Sister Cities Teach Abroad Program',
          location: 'Himeji, Japan',
          dates: 'January 2014 - December 2015'
        },
        {
          title: 'Teacher',
          company: 'Peoria Unified School District',
          location: 'Peoria, AZ',
          dates: 'December 2010 - May 2013'
        }
      ],
      education: [
        {
          program: 'Web Development Full Stack Immersive Program',
          school: 'Galvanize',
          location: 'Phoenix, AZ',
          date: 'February 2017 - July 2017',
        },
        {
          program: 'B.A. Education',
          school: 'Arizona State University',
          location: 'Tempe, AZ',
          date: 'August 2007 - December 2010',
          honors: 'Summa Cum Laude'
        }
      ]
    }
  }
}
</script>

<style lang="css" scoped>

  #experience {
    margin: 50px 0;
  }

  #education {
    margin-bottom: 50px;
  }

  .role h3 {
    /*font-size: 1.7em;*/
    font-family: 'Metrophobic', Helvetica, Arial, sans-serif;
    /*font-family: 'Muli', sans-serif;
    font-family: 'Nunito', sans-serif;*/
  }

  .mb-2 {
    margin: 0 auto;
  }

</style>
