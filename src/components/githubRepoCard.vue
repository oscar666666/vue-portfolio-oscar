<template>
  <div id="githubrepocard">
    <div class="container">
      <b-row>
        <b-col></b-col>
        <b-col sm="8">
          <b-row cols="2">
            <div
              class="repocard"
              v-for="(repo, index) in repos"
              v-bind:key="repo.id"
            >
              <b-col>
                <div id="name">
                  <a :href="repo.html_url">
                    <svg
                      xmlns="http://www.w3.org/2000/svg"
                      viewBox="0 0 24 24"
                      width="24"
                      height="24"
                    >
                      <path
                        fill="#8b949e"
                        fill-rule="evenodd"
                        d="M3 2.75A2.75 2.75 0 015.75 0h14.5a.75.75 0 01.75.75v20.5a.75.75 0 01-.75.75h-6a.75.75 0 010-1.5h5.25v-4H6A1.5 1.5 0 004.5 18v.75c0 .716.43 1.334 1.05 1.605a.75.75 0 01-.6 1.374A3.25 3.25 0 013 18.75v-16zM19.5 1.5V15H6c-.546 0-1.059.146-1.5.401V2.75c0-.69.56-1.25 1.25-1.25H19.5z"
                      ></path>
                      <path
                        d="M7 18.25a.25.25 0 01.25-.25h5a.25.25 0 01.25.25v5.01a.25.25 0 01-.397.201l-2.206-1.604a.25.25 0 00-.294 0L7.397 23.46a.25.25 0 01-.397-.2v-5.01z"
                      ></path></svg
                    >{{ repo.name }}
                  </a>
                </div>
                <div id="description">{{ repo.description }}{{ index }}</div>
                <div id="bottom">
                  <span
                    class="repo-language-color"
                    :style="{ background: languageColor(repo.language) }"
                  ></span>
                  {{ repo.language }}
                  <!-- svg github star-->
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 16 16"
                    width="16"
                    height="16"
                  >
                    <path
                      fill="#8b949e"
                      fill-rule="evenodd"
                      d="M8 .25a.75.75 0 01.673.418l1.882 3.815 4.21.612a.75.75 0 01.416 1.279l-3.046 2.97.719 4.192a.75.75 0 01-1.088.791L8 12.347l-3.766 1.98a.75.75 0 01-1.088-.79l.72-4.194L.818 6.374a.75.75 0 01.416-1.28l4.21-.611L7.327.668A.75.75 0 018 .25zm0 2.445L6.615 5.5a.75.75 0 01-.564.41l-3.097.45 2.24 2.184a.75.75 0 01.216.664l-.528 3.084 2.769-1.456a.75.75 0 01.698 0l2.77 1.456-.53-3.084a.75.75 0 01.216-.664l2.24-2.183-3.096-.45a.75.75 0 01-.564-.41L8 2.694v.001z"
                    ></path></svg
                  >{{ repo.stargazers_count }}
                  <!-- github fork-->
                  <svg
                    xmlns="http://www.w3.org/2000/svg"
                    viewBox="0 0 16 16"
                    width="16"
                    height="16"
                  >
                    <path
                      fill="#8b949e"
                      fill-rule="evenodd"
                      d="M5 3.25a.75.75 0 11-1.5 0 .75.75 0 011.5 0zm0 2.122a2.25 2.25 0 10-1.5 0v.878A2.25 2.25 0 005.75 8.5h1.5v2.128a2.251 2.251 0 101.5 0V8.5h1.5a2.25 2.25 0 002.25-2.25v-.878a2.25 2.25 0 10-1.5 0v.878a.75.75 0 01-.75.75h-4.5A.75.75 0 015 6.25v-.878zm3.75 7.378a.75.75 0 11-1.5 0 .75.75 0 011.5 0zm3-8.75a.75.75 0 100-1.5.75.75 0 000 1.5z"
                    ></path></svg
                  >{{ repo.watchers_count }}
                </div>
              </b-col>
            </div>
          </b-row>
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
#githubrepocard {
  height: 100%;
  background-color: #1b2431;
}
.repocard {
  margin: 0rem;
  padding: 1.125rem;
  border-radius: 0.3rem;
  border: 2px solid;
  border-color: #2780b4;
  box-shadow: 3px 3px #0b42b8;
  display: grid;
  row-gap: 0.5rem;
  align-content: space-between;
  color: #0d1117;
}
.repocard:hover{
  box-shadow: 0px 0px 0;


}
#name {
  font-family: -apple-system, BlinkMacSystemFont, Segoe UI, Helvetica, Arial,
    sans-serif, Apple Color Emoji, Segoe UI Emoji, Segoe UI Symbol !important;
  margin: 0;
  font-weight: 550;
  font-size: 1.4rem;
  letter-spacing: -0.075rem;
  overflow-wrap: anywhere;
  color: #287272;
  line-height: 1.5;
  text-align: left;
}
#description {
  line-height: 1.75;
  margin: 0;
  text-align: left;
  color: #8b949e;
}
#bottom {
  margin: 0;
  text-align: left;
  color: #8b949e;
}
.repo-language-color {
  filter: brightness(125%) !important;
  border-radius: 50%;
  display: inline-block;
  height: 12px;
  position: relative;
  top: 2px;
  width: 12px;
}
.active {
  box-shadow: 0px 0px 0;
}
</style>
<script>
import plangcolors from "./json/programming-languages-colors.json";
import axios from "axios";

export default {
  name: "githubrepocard",
  data() {
    return { repos: null, hover: false, plangcolors: plangcolors };
  },
  components: {},
  methods: {
    languageColor(language) {
      return this.plangcolors[language].color; // pick up the right color by language
    },
  },
  mounted() {
    axios
      .get("https://api.github.com/users/oscar666666/repos")
      .then((response) => (this.repos = response.data));
  },
};
</script>
