<template>
  <div id="experience">
    <div class="container">
      <br /><br /><br />
      <br />
      <b-row align-h="center">
        <b-col sm="0"> </b-col>

        <b-col sm="9">
          <h2 id="section-title">1. Experience</h2>

          <br />

          <vue-timeline-update
            v-for="job in jobs"
            :key="job.id"
            :date="job.date"
            :title="job.title"
            :description="job.description"
            :thumbnail="job.thumbnail"
            :category="job.category"
            :icon="job.icon"
            :color="job.color"
            is-last
          />
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
#experience {
  height: 100%;
  background-color: #1b2431;
}
</style>
<script>
export default {
  name: "experience",
  components: {},
  data() {
    return {
      jobs: [
        {
          date: "2021-05-06",
          title: "Under Development",
          description:
            "New updates coming soon",
          thumbnail: "https://raw.githubusercontent.com/oscar666666/vue-portfolio-oscar/main/src/assets/rh3wh.jpg",
          category: "announcement",
          icon: "code",
          color: "blue",
        },
        {
          date: "2021-04-22",
          title: "Food Counter Attendant @Tim Hortons",
          description:
            "<p>Job duties:</p>\
            <ul>\
            <li>Brew coffee and tea for customers </li>\
            <li>Take customers' orders</li>\
            <li>Pack Timbits and Donuts as per customers’ order</li>\
            <li>Remove garbage and refill Sanitazer in kitchen area</li>\
            <li>Sanitize tables in eating establishments </li>\
            </ul> \
          ",
          thumbnail: "https://raw.githubusercontent.com/oscar666666/vue-portfolio-oscar/main/src/assets/jco50158061-1.jpg",
          category: "Full-Time",
          icon: "local_cafe",
          color: "red",
        },
        {
          date: "2020-05-01",
          title: "General Labour @Great Asian Market",
          description:
            "<p>Job duties:</p>\
            <ul>\
            <li>Maintain max customer capacity in store </li>\
            <li>Restock inventories of frozen goods</li>\
            <li>Provide information about items and make buying suggestions</li>\
            <li>Clean shopping carts and fridge handles in response to Covid-19</li>\
            <li>Pack variety of vegetables and fruits </li>\
            </ul> \
          ",
          thumbnail: "https://raw.githubusercontent.com/oscar666666/vue-portfolio-oscar/main/src/assets/DSC_0154.JPG",
          category: "Part-Time",
          icon: "local_grocery_store",
          color: "white",
        },
      ],
    };
  },
};
</script>
