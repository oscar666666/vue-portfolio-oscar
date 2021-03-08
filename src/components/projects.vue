<template>
  <div id="projects">
    <div class="container">
      <br /><br /><br />
      <br />
      <b-row align-h="center">
        <b-col sm="6">
          <h2 id="section-title">2. Projects</h2>
        </b-col>
        <b-col sm="3"></b-col>
      </b-row>
      <b-row align-h="center">
        <b-col sm="8">
      <b-card bg-variant="dark" border-variant="info" text-variant="white" title="Card Title">
        <b-card-text>
{{ info }}        </b-card-text>
        <b-button pill class="btn btn-theme float-right" size="sm" href="#">Go somewhere</b-button>
      </b-card>
              </b-col>

      </b-row>
    </div>
  </div>
</template>

<style>
html,
body {
  height: 100%;
  width: 100%;
  margin: 0;
}
h1 {
  text-align: left;
}
#introduce-text {
  font-size: 20px;
  color: #c4babe;
}
#contactme {
  color: #2da07a;
}
#section-title {
  color: #2da07a;
  text-align: left;
}
.container {
  font-weight: normal;
}
#header {
  height: 15vh;
}
#projects {
  height: 100vh;
  background-color: #343a40;
}

</style>
<script>
import axios from 'axios'
export default {
  name: "projects",
  data() {
    return {
      info: null,
    };
  },
  mounted () {
    axios
      .get('https://api.github.com/users/oscar666666/repos')
      .then(response => (this.info = response))
  },
  components: {},
};
</script>
