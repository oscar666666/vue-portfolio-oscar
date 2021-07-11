<template>
  <div id="skills">
    <div class="container">
      <br /><br /><br />
      <br />
      <b-row align-h="center">
        <b-col sm="0"> </b-col>

        <b-col sm="9">
          <h2 id="section-title">3. Skills</h2>
          <br />
      <br />
          <div>
            <VueSlickCarousel  v-bind="settings">
              <div v-for="(images, index) in skillsimg" :key="index">
                <i id="devicon" :class="images.image"  width="100px"
              height="100px"></i>
                <!--<img :src="images.image" width="100px"
              height="100px" alt="" />-->
              </div>
            </VueSlickCarousel>
            
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
  text-align: left;
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
#skills {
  height: 100%;
  background-color: #1b2431;
}
#devicon {
  font-size: 5rem
}
</style>
<script>
import VueSlickCarousel from "vue-slick-carousel";
// optional style for arrows & dots
import "vue-slick-carousel/dist/vue-slick-carousel.css";
import "vue-slick-carousel/dist/vue-slick-carousel-theme.css";
export default {
  name: "skills",
  data() {
    return {
      skillsimg: [
        {
          image:
            "devicon-android-plain colored",
        },
        {
          image:
            "devicon-cplusplus-plain colored",
        },{
          image:
            "devicon-css3-plain colored",
        },{
          image:
            "devicon-django-plain colored",
        },{
          image:
            "devicon-git-plain colored",
        },{
          image:
            "devicon-html5-plain colored",
        },{
          image:
            "devicon-java-plain colored",
        },{
          image:
            "devicon-javascript-plain colored",
        },{
          image:
            "devicon-mysql-plain colored",
        },{
          image:
            "devicon-php-plain colored",
        },{
          image:
            "devicon-python-plain colored",
        },{
          image:
            "devicon-vuejs-plain colored",
        },
      ],
      settings: {
        centerMode: true,
        centerPadding: "20px",
        focusOnSelect: true,
        infinite: true,
        slidesToShow: 5,
        speed: 500,
      },
    };
  },
  components: { VueSlickCarousel,    
  },
};
</script>
