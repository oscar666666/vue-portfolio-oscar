<template>
  <div>
    <b-navbar class="fixed-top" type="dark" variant="dark">
      <b-navbar-brand href="/">
        <img src="../assets/home-5-fill.png" class="d-inline-block align-top" />
        Home
      </b-navbar-brand>
      <!-- Left aligned nav items -->
      <b-navbar-nav>
        <a href="/files/Oscar-Lou-Resume-2021.pdf" target="_blank"
          ><b-button variant="outline-light">Resume </b-button></a
        >
        <!--<b-nav-item href="#about">About</b-nav-item>-->
      </b-navbar-nav>
      <!-- Right aligned nav items -->
      <b-navbar-nav class="ml-auto">
        <b-nav-item href="#about">0.About</b-nav-item>

        <b-nav-item href="#experience">1.Experience</b-nav-item>

        <b-nav-item href="#projects">2.Projects</b-nav-item>

        <b-nav-item href="#skills">3.Skills</b-nav-item>
      </b-navbar-nav>
    </b-navbar>
  </div>
</template>
