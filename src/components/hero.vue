<template>
  <div id="hero">
      <br /><br /><br />
      <br />
          <div class="container">

      <b-row align-h="left">
        <div id="heroText">
            <h1> Oscar Lou</h1>
            <p>Software Developer</p>
        </div>
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

#heroText {
    margin: 0 0 30px 4px;
    text-align: top;
    color: #5c8083;
    font-family: Monospace;
    font-weight: 400;
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
#hero {
  min-height: 100vh;
  height: 100vh;
  display: flex;
  align-items: center;
  border-bottom: 0px;
  background: url("../assets/PXL_20210303_050253767.jpg");
  background-position: center;
  background-repeat: no-repeat;
  background-attachment: fixed;/*remove this for ios*/
  background-size: 100% 100%;
  font-weight: 400;
  padding: 0rem 5.6rem;
  margin-bottom: 0;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
  z-index: -1;
  background-color: #343a40;
}

</style>
<script>
export default {
  name: "hero",
  data() {
    return {};
  },
  components: {},
};
</script>
