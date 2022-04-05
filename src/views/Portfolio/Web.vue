<template>
  <v-container grid-list-xl>
    <h2 class="pl-4">
      <span>Web</span>
      <span class="blue--text">Portfolio</span>
    </h2>
    <v-layout row justify-center align-center wrap class="mt-4 pt-2">
      <v-dialog
        v-model="project.dialog"
        lazy
        max-width="1000"
        v-for="project in projects"
        :key="project.title"
      >
        <template v-slot:activator="{ on }">
          <v-flex xs12 sm6 md4 lg4 xl4 v-on="on">
            <v-card hover flat color="transparent">
              <v-img
                :src="project.poster"
                :alt="project.title"
                height="230"
                lazy-src="https://cdn.dribbble.com/users/503653/screenshots/3143656/fluid-loader.gif"
              ></v-img>
              <v-card-title primary-title class="justify-center">{{project.title}}</v-card-title>
            </v-card>
          </v-flex>
        </template>
        <v-card v-if="project.dialog">
          <v-img :src="project.poster"></v-img>
          <v-card-text>
            <h3 class="headline mb-0">
              <span>Technology</span>
            </h3>
            <v-chip color="blue" text-color="white">{{project.tech.tech1}}</v-chip>
            <v-chip color="blue" text-color="white">{{project.tech.tech2}}</v-chip>
            <v-chip color="blue" text-color="white">{{project.tech.tech3}}</v-chip>
            <v-chip color="blue" text-color="white">{{project.tech.tech4}}</v-chip>
          </v-card-text>
          <v-card-actions>
            <v-btn flat large dark color="blue" :href="project.git" target="_blank">
              <v-icon left>fab fa-github</v-icon>GitHub
            </v-btn>
            <v-btn large flat dark color="blue" :href="project.demo" target="_blank">
              <v-icon left>fas fa-desktop</v-icon>Demo
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-dialog>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  metaInfo: {
    title: "Web Portfolio",
    titleTemplate: "%s ← Eldin's Space",
    meta: [
      { name: "viewport", content: "width=device-width, initial-scale=1" },
      {
        name: "description",
        content:
          "Sulai Sivadel's Web Portfolio Vue Vue.js Nuxt Nuxt.js HTML CSS Vuetify Axios GraphQL JavaScript Web Developer Front-End Frontend Designer App Responsive"
      },
      { charset: "utf-8" },
      { property: "og:title", content: "Sulai Sivadel" },
      { property: "og:site_name", content: "Sulai Sivadel" },
      { property: "og:type", content: "website" },
      { property: "og:url", content: "https://www.sulai.me" },
      {
        property: "og:image",
        content: "https://i.imgur.com/Dcz2PGx.jpg"
      },
      {
        property: "og:description",
        content:
          "Sulai Sivadel Web Portfolio Vue Vue.js HTML CSS Vuetify Axios GraphQL JavaScript Web Developer Front-End Frontend Designer App Responsive"
      }
    ]
  },
  data() {
    return {
      dialog: false,
      projects: [
         {
          dialog: false,
          title: "Party Dash",
          git: "",
          demo: "https://www.partydash.com/",
          tech: {
            tech1: "VueJs",
            tech2: "JavaScript",
            tech3: "CSS",
            tech4: "Markdown"
          },
          poster: "https://i.imgur.com/5uBCmox.png"
        },
        {
          dialog: false,
          title: "Mayapple Center for the Arts & Humanites",
          git: "",
          demo: "https://www.mayapplecenter.org/",
          tech: {
            tech1: "Wordpress",
            tech2: "HTML",
            tech3: "",
            tech4: ""
          },
          poster: "https://i.imgur.com/6GR6DC5.jpg"
        },
        {
          dialog: false,
          title: "Developer for michelleslater.com",
          git: "",
          demo: "https://michelleslater.com/",
          tech: {
            tech1: "Wordpress",
            tech2: "HTML",
            tech3: "",
            tech4: ""
          },
          poster: "https://i.imgur.com/TSWhSC3.jpg"
        },
        {
          dialog: false,
          title: "JohnDavidWest.com",
          git: "",
          demo: "https://www.johndavidwest.com/",
          tech: {
            tech1: "HTML",
            tech2: "CSS",
            tech3: "",
            tech4: ""
          },
          poster: "https://i.imgur.com/cv4WrDO.jpg"
        },
        {
          dialog: false,
          title: "Sulai.me",
          git: "https://github.com/Sulai3030/portfolio10/tree/master",
          demo: "https://www.sulai.me",
          tech: {
            tech1: "VUEJs",
            tech2: "CSS",
            tech3: "Javascript",
            tech4: ""
          },
          poster: "https://i.imgur.com/irETqQt.jpg"
        },
        {
          dialog: false,
          title: "GraphQL-Practice",
          git: "https://github.com/Sulai3030/graphql-practice",
          demo: "",
          tech: {
            tech1: "GraphQL",
            tech2: "",
            tech3: "HTML",
            tech4: "JavaScript"
          },
          poster: "https://imgur.com/t/graph/1X8LpaQ"
        },
        {
          dialog: false,
          title: "RuneSkype",
          git: "https://github.com/Sulai3030/RuneSkype",
          demo: "https://github.com/Jroze88/RuneSkype",
          tech: {
            tech1: "ReactJS",
            tech2: "Firebase",
            tech3: "Express",
            tech4: ""
          },
          poster: "https://i.imgur.com/wK5dqP7.png"
        },
        {
          dialog: false,
          title: "Riders Share Newsleter",
          git: "",
          demo: "https://imgur.com/zTMJhGk",
          tech: {
            tech1: "HTML",
            tech2: "CSS",
            tech3: "MailChimp",
            tech4: "JavaScript"
          },
          poster: "https://i.imgur.com/zTMJhGk.jpg"
        },
        {
          dialog: false,
          title: "My Old Web Portfolio",
          git: "https://github.com/EldinZaimovic/EldinZaimovic.github.io",
          demo: "https://eldinzaimovic.github.io/index.html",
          tech: {
            tech1: "HTML",
            tech2: "CSS",
            tech3: "JavaScript",
            tech4: "jQuery"
          },
          poster: "https://i.imgur.com/AW7CXD5.jpg"
        }
      ]
    };
  }
};
</script>

<style  scoped>
</style>