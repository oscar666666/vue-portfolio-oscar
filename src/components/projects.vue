<template>
  <div id="projects">
    <div class="container">
        <br /><br /><br />
      <br />
      <b-row>
        <b-col></b-col>
        <b-col cols="10"
          ><h2 id="section-title">2. Projects</h2>
          </b-col>
          <b-col></b-col>
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
export default {
  name: "about",
  data() {
    return {
      isHovered0: false,
      isHovered1: false,
      isHovered2: false,
      isHovered3: false,
    };
  },
  methods: {
    handleHover0(hovered) {
      this.isHovered0 = hovered;
    },
    handleHover1(hovered) {
      this.isHovered1 = hovered;
    },
    handleHover2(hovered) {
      this.isHovered2 = hovered;
    },
    handleHover3(hovered) {
      this.isHovered3 = hovered;
    },
  },
  components: {},
};
</script>
