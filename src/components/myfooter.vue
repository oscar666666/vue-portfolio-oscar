<template>
  <div id="myfooter">
    <div class="container">
      <br /><br />
      <b-row align-h="center">
        <b-col sm="6" align="left">
          <h2 id="section-title">Oscar Lou</h2>
          <p id="footer-text">
            I'm currently looking for any new opportunities. Please hit me up if
            you have a position that might be a fit for me. I will get back to
            you as soon as possible!
          </p>
        </b-col>
        <b-col sm="4" align="left">
          <h2 id="section-title">Contact me:</h2>
          <p id="footer-text">
            <svg-icon class="icon" type="mdi" :path="path"></svg-icon>
            sseoscar4work@gmail.com
          </p>
          <a href="https://github.com/oscar666666" id="footer-text"
            ><svg-icon class="icon" type="mdi" :path="path2"></svg-icon> Github
            Link</a
          >
        </b-col>
        <b-col sm="2">
          <h2 id="section-title">Resources</h2>
        </b-col></b-row
      >
      <hr class="footerhr" />
      <p>© 2021 Oscar Lou All rights reserved.</p>
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

.container {
  font-weight: normal;
}
#myfooter {
  height: 100%;
  background-color: #343a40;
}
hr.footerhr {
  border: 3px solid rgb(43, 66, 70);
  border-radius: 2px;
}
.icon {
  width: 3em;
  display: inline;
  margin-right: 2px;
  position: relative;
  top: 0em;
}
#footer-text {
  font-size: 18px;
  color: #aedfd8;
}
</style>
<script>
import { mdiEmail } from "@mdi/js";
import { mdiGithub } from "@mdi/js";
import SvgIcon from "@jamescoyle/vue-icon";
export default {
  name: "myfooter",
  data() {
    return {
      path: mdiEmail,
      path2: mdiGithub,
    };
  },
  components: { SvgIcon },
};
</script>
