<template>
  <v-timeline>
    <v-banner
      color="accent"
      elevation="24"
      rounded
      shaped
      sticky>
      <h2>APPLICATIONS BUILT</h2>
    </v-banner>
    <v-timeline-item
      color="red lighten-2"
      large
    >
      <template v-slot:opposite>
        <span><h2>Project 1. Party Dash </h2><a href="https://partydash.com/">https://partydash.com/</a></span>
      </template>
      <v-card class="elevation-2">
        <v-card-title class="text-h5">
          Front-End Design
        </v-card-title>
        <v-card-text>
          We built Party Dash with a simple goal in mind: to help party hosts plan parties more easily
        </v-card-text>
        <v-card-text>
          Responsibilities: Follow design specs handed down from site owner. Used CSS and HTML to create inviting website
        </v-card-text>
        <v-card-text>
          Technologies used: HTML, CSS, Bootstrap
        </v-card-text>
      </v-card>
    </v-timeline-item>
    <v-timeline-item
      color="red lighten-2"
      large>
      <template v-slot:opposite>
        <span><h2>Project 2. RuneSkype </h2><a href="https://runeskype.herokuapp.com/play">https://runeskype.herokuapp.com/play</a></span>
      </template>
      <v-card class="elevation-2">
        <v-card-title class="text-h5">
          Front-end design, Linting, cleaning up frontend and backend code and making sure both sides work together.
        </v-card-title>
        <v-card-text>
          RuneSkype is the newest way for friends to interact while playing your favorite Role Playing Game (RPG) RuneSkype. Playing RuneSkype is easy, just download a copy from our homepage or our repo:
        </v-card-text>
        <v-card-text>
          Responsibilities:  Wrote clean, presentable code. Kept group on time and on track to present at Project Demo Day
        </v-card-text>
        <v-card-text>
          Technologies used: ReactJS, ChanceJS, Node, Express, Firebase, Twilio-Video, Twilio, WebRTC, Axios. Express, Faker, jQuery, React-dnd, React-dnd-html5-backend,React-dom, React-draggable, React-router-dom, Webpack-dev-middleware, Webpack hot-middleware
        </v-card-text>
      </v-card>
    </v-timeline-item>
    <v-timeline-item
      color="red lighten-2"
      large>
      <template v-slot:opposite>
        <span><h2>Project 3. The GOAT Voter App | </h2><a href="http://www.goatvoter.org">https://www.goatvoter.org/</a></span>
      </template>
      <v-card class="elevation-2">
        <v-card-title class="text-h5">
          Front-End Design, created the color scheme and front-end components
        </v-card-title>
        <v-card-text>
          The GOAT Voter App is a one-stop platform where voters can access information about candidates running for political offices anywhere in the United States. The GOAT Voter App streamlines information and increases voter participation.
        </v-card-text>
        <v-card-text>
          Responsibilities:  Wrote clean, presentable code. Kept group on time and on track to present at Project Demo Day
        </v-card-text>
        <v-card-text>
          By entering their zip code in a search field, users will be able to search and access detailed information about all candidates running for election in their district. In addition, users can enter their address to find out where their nearest polling site is located and request transportation on election day.
        </v-card-text>
        <v-card-text>
          Technologies used: JavaScript, Handlebars, Bootstrap, CSS Parallax, Node.js, Express, Sequelize, Google Civic Information API, Heroku
        </v-card-text>
      </v-card>
    </v-timeline-item>
    <v-timeline>
    <v-banner
      color="accent"
      elevation="24"
      rounded
      shaped
      sticky>
      <h2>RELEVANT EXPERIENCE</h2>
    </v-banner>
    <v-card
      class="mx-auto"
      max-width="800"
      tile
      elevation-2>
      <v-list-item three-line>
        <v-list-item-content>
          <v-card-title class="text-h5">Mayapple Center for the Arts and Humanities| www.mayapple.org</v-card-title>
          <v-card-title class="text-h5">Webmaster</v-card-title>
          <v-card-title class="text-h5">
            Updated and maintained website (Drupal 7 platform), creating links between Mayapple’s homepage and their yearly summer program at Sarah Lawrence College. Added, removed, and refined content for Events, Faculty, Executive Staff, Executive Board, and Advisory Board pages.      
          </v-card-title> 
          <v-list-item-subtitle>
            <i>Key Accomplishments:</i>
          </v-list-item-subtitle>
          <v-card-title class="text-h5">Removed departed Advisory Board members from Advisory Board page and added new Advisory Board Members </v-card-title>         
          <v-card-title class="text-h5">Input new faculty on Faculty page and Executive Board listing and names.</v-card-title>
          <v-card-title class="text-h5">Communicated foundation’s message through updates on homepage about mission, events, enrollment opportunities and scholarships</v-card-title>
       </v-list-item-content>
     </v-list-item>
    </v-card>
  </v-timeline>
</template>

<script>
export default {
  metaInfo: {
    title: "Resume",
    titleTemplate: "%s ← Sulai Sivadel",
    meta: [
      { name: "viewport", content: "width=device-width, initial-scale=1" },
      {
        name: "description",
        content:
          "VueJS HTML CSS JavaScript Design Adobe XD Photoshop Coding Skills Resume Work Web Developer Front-End"
      },
      { charset: "utf-8" },
      { property: "og:title", content: "Sulai Sivadel" },
      { property: "og:site_name", content: "Sulai's Space" },
      { property: "og:type", content: "website" },
      { property: "og:url", content: "https://www.sulai.me" },
      {
        property: "og:image",
        content: "https://i.imgur.com/Dcz2PGx.jpg"
      },
      {
        property: "og:description",
        content:
          "Vue NUXT HTML CSS JavaScript Design Adobe XD Photoshop Coding Skills Resume Work Web Developer Front-End"
      }
    ]
  },
  data() {
    return {
      value: 0,
      buffer1: 0,
      buffer2: 0,
      buffer3: 0,
      buffer4: 0,
      buffer5: 0,
      buffer6: 0,
      bufferValue: 100,
      interval: 0
    };
  },
  mounted() {
    this.startBuffer();
  },

  beforeDestroy() {
    clearInterval(this.interval);
  },

  methods: {
    startBuffer() {
      this.interval = setInterval(() => {
        this.buffer1 = 90;
        this.buffer2 = 85;
        this.buffer3 = 80;
        this.buffer4 = 80;
        this.buffer5 = 90;
        this.buffer6 = 70;
      }, 800);
    }
  }
};
</script>
<style >
</style>

