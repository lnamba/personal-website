<template>
  <div id="contact">
    <div class="col-md-12">
      <h1>Contact</h1>
      <h4>Stay Connected.</h4>
      <h2 id="email">lnnamba@gmail.com</h2>
      <a href="https://github.com/lnamba"><img class="icon" src="../assets/GitHub.png" alt="GitHub"></a>
      <a href="https://www.linkedin.com/in/laurennamba/"><img class="icon" src="../assets/linkedin.png" alt="LinkedIn" id="in"></a>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {

    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

  #contact {
    padding: 50px 0;
    background-color: #000;
    color: #FFF;
  }

  #email {
    margin-top: 50px;
  }

  .icon {
    margin-top: 20px;
    height: 40px;
  }

  #in {
    margin-left: 20px;
  }

</style>
