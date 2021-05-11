<template>
  <div id="myfooter">
    <div class="container">
      <br><br>
      <b-row align-h="center">
        <b-col sm="6">
          <h2 id="section-title">Oscar Lou</h2>
        </b-col>
        <b-col sm="3">
          <h2 id="section-title">Contact me:</h2>
          <svg-icon type="mdi" :path="path"></svg-icon>
        </b-col>
        <b-col sm="3">
          <h2 id="section-title">footer</h2>
        </b-col></b-row>
        <hr class="footerhr">
        <p> © 2021 Oscar Lou All rights reserved. </p>
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
</style>
<script>
import { mdiEmail } from '@mdi/js'; 
import SvgIcon from '@jamescoyle/vue-icon'
export default {
  name: "myfooter",
  data() {
    return {
            path: mdiEmail,
        };
  },
  components: {    SvgIcon
},
};
</script>
