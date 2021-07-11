<template>
  <div id="eduandcert">
    <div class="container">
      <br /><br /><br />
      <br />
      <b-row align-h="center">
        <b-col sm="0"> </b-col>

        <b-col sm="9">
          <h2 id="section-title">4. Education & Certification</h2>

          <br />
          <div class="educard" v-for="cert in certs" :key="cert.certname">
            <div class="icon">
              <img :src="require(`@/assets/${cert.icon}.jpg`)" class="icon"/>
            </div>
            <div class="word">
              <div id="certname">
                {{ cert.certname }}
              </div>
              <div id="subtitle">
                {{ cert.subtitle }}
              </div>
              <div id="time">
                {{ cert.time }}
              </div>
            </div>
          </div>
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
  color: #81869c;
}
.container {
  font-weight: bold;
}
#header {
  height: 15vh;
}
#eduandcert {
  height: 100%;
  background-color: #1b2431;
}
.educard {
  display: flex;
  margin: 8px;
}
.icon {
  vertical-align: middle;
  width: 50px;
  height: 50px;
  border-radius: 50%;
  flex: 0;
  margin-right: 5px;
}
#certname {
  font-family: -apple-system, BlinkMacSystemFont, Segoe UI, Helvetica, Arial,
    sans-serif, Apple Color Emoji, Segoe UI Emoji, Segoe UI Symbol !important;
  margin: 5px;

  font-weight: 550;
  font-size: 1.4rem;
  letter-spacing: -0.075rem;
  overflow-wrap: anywhere;
  color: #287272;
  line-height: 1.3;
  text-align: left;
}
#subtitle {
  margin: 5px;

  font-size: 18px;
  font-weight: 700;
  color: #6ec5b8;
  text-align: left;
}
#time {
  margin: 5px;

  font-weight: 700;
  font-size: 16px;
  color: #385761;
  text-align: left;
}
</style>
<script>
export default {
  name: "eduandcert",
  components: {},
  data() {
    return {
      certs: [
        {
          icon: "UR_Logo_Secondary_Stacked Full_Colour_RGB",
          certname: "University of Regina",
          subtitle: "Bachelor of Applied Science - Software Systems Engineering",
          time: "2015-2020",
        },
        {
          icon:
            "390EFE04A66323AA4F38BEF156353B9C20180509092121_o",
          certname:
            " Association of Professional Engineers and Geoscientists of Saskatchewan (APEGS)",
          subtitle: "Engineer-In-Training",
          time: "2021-2022",
        },
      ],
    };
  },
};
</script>
