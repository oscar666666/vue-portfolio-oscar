<template>
  <div id="app">
        <loading-screen :is-loading="isLoading"></loading-screen>
    <navigation/>
    <hero/>
    <about/>
    <experience/>
    <projects/>
    <skills/>
    <router-view/>
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #1b2431;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
<script>
import Navigation from './components/navigation.vue' //import the component
import Hero from './components/hero.vue' //import the component
import About from './components/about.vue' //import the component
import Experience from './components/experience.vue' //import the component
import Projects from './components/projects.vue' //import the component
import Skills from './components/skills.vue' //import the component
import Loader from "./components/Loader";
export default {
  name: 'App',
  components: {
        'loading-screen': Loader,
    Navigation,  //instantiate it here
    Hero,
    About,
    Experience,
    Projects,
    Skills
  },
  data(){
    return{
      isLoading: true
    }
  },
  mounted () {
    setTimeout(() => {
      this.isLoading = false
    }, 2500)
  }
}
</script>