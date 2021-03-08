<template>
  <div id="about">
    <div class="container">
      <br /><br /><br />
      <br />
      <!-- this is covered by top navbar -->
      <b-row align-h="center">
        <b-col sm="6">
          <h2 id="section-title">0. About me</h2>
          <br />
          <p id="introduce-text" align="left">
            Hello! I'm Oscar, a software developer. I am extremely passionate
            about software development and applies scientific knowledge to
            software projects. I take great ownership of projects and
            understands the importance of communicating with colleagues and
            users during the life cycle of software projects.
          </p>
          <br /><br />
        </b-col>

        <b-col sm="3">
          <b-img
            src="../assets/693952main_pia15817-full_full.jpg"
            rounded
            fluid-grow
            alt="profile image"
          ></b-img>
        </b-col>
      </b-row>

      <b-row align-h="left">
        <b-col sm="2"></b-col>
        <b-col sm="1">
          <div v-b-hover="handleHover0">
            <a href="mailto:sseoscar4work@gmail.com">
              <b-icon
                v-if="isHovered0"
                icon="mailbox"
                alt="Email"
                style="width:42px;height:42px;"
                color="cyan"
              >
              </b-icon>
              <b-icon
                v-else
                icon="mailbox"
                alt="Email"
                style="width:42px;height:42px;"
                color="black"
              >
              </b-icon>
            </a>
          </div>
        </b-col>
        <b-col sm="1">
          <div v-b-hover="handleHover1">
            <a href="https://github.com/oscar666666">
              <b-icon
                v-if="isHovered1"
                icon="github"
                alt="Github"
                style="width:42px;height:42px;"
                color="cyan"
              >
              </b-icon>
              <b-icon
                v-else
                icon="github"
                alt="Github"
                style="width:42px;height:42px;"
                color="black"
              >
              </b-icon>
            </a>
          </div>
        </b-col>
        <b-col sm="1">
          <div v-b-hover="handleHover2">
            <a href="https://www.linkedin.com/in/sse-oscar-lou/">
              <b-icon
                v-if="isHovered2"
                icon="linkedin"
                alt="Linkedin"
                style="width:42px;height:42px;"
                color="cyan"
              >
              </b-icon>
              <b-icon
                v-else
                icon="linkedin"
                alt="Linkedin"
                style="width:42px;height:42px;"
                color="black"
              >
              </b-icon>
            </a>
          </div>
        </b-col>
        <b-col sm="1">
          <div v-b-hover="handleHover3">
            <a href="https://leetcode.com/oscar88feichang6/">
              <img
                v-if="isHovered3"
                src="../assets/cyan-leetcode-icon.jpg"
                alt="Leetcode"
                style="width:42px;height:42px;"
                color="cyan"
              />

              <img
                v-else
                src="../assets/cib-leetcode.svg"
                alt="Leetcode"
                style="width:42px;height:42px;"
                color="black"
              />
            </a>
          </div>
        </b-col>


      </b-row>
              <br /><br /><br />
        <br />
    </div>
  </div>
</template>

<style>
html,
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
#about {
  height: 100%;
  vertical-align: top;
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
