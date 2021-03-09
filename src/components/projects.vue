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

          <b-card
            v-for="repo in repos"
            v-bind:key="repo.id"
            :title="repo.name"
            :sub-title="repo.language"
            bg-variant="dark"
            border-variant="info"
            text-variant="white"
          >
            <b-card-text> {{ repo.description }} </b-card-text>
            <b-button pill class="btn btn-theme float-right" size="sm" href="#"
              >{{repo.id}}</b-button
            >
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
  height: 15%;
}
#projects {
  height: 100%;
  background-color: #343a40;
}
</style>
<script>
import axios from "axios";
export default {
  name: "projects",
  data() {
    return {
      repos: null,
    };
  },
  mounted() {
    axios
      .get("https://api.github.com/users/oscar666666/repos")
      .then((response) => (this.repos = response.data));
  },
  components: {},
};
</script>
