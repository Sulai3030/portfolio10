<template>
  <v-container grid-list-xl>
    <v-layout row justify-center align-center wrap class="mt-4 pt-2">
      <v-flex xs12 sm12 md12 lg12 xl12>
        <h2 class="pl-4">
          <span class="blue--text">My</span>
          <span class="blue--text">Services</span>
        </h2>
      </v-flex>
      <v-flex v-for="service in services" :key="service.src" xs6 sm3 md3 lg3 xl3>
        <v-card hover flat color="transparent" :style="{'cursor':'context-menu'}">
          <v-card-title></v-card-title>
          <v-img
            :src="service.src"
            height="100"
            aspect-ratio="2.75"
            :alt="'Eldin do '+service.title"
            lazy-src="https://cdn.dribbble.com/users/503653/screenshots/3143656/fluid-loader.gif"
            contain
          ></v-img>
          <v-card-title class="justify-center">
            <v-flex text-xs-center subheading font-weight-bold>{{service.title}}</v-flex>
          </v-card-title>
        </v-card>
      </v-flex>
      <v-flex xs12 sm12 md12 lg12 xl12>
        <h2 class="pl-4">
          <span class="blue--text">My</span>
          <span class="blue--text">Clients</span>
        </h2>
      </v-flex>

      <v-flex v-for="client in clients" :key="client.src" xs6 sm4 md3 lg2 xl2>
        <v-card flat :href="client.href" target="_blank" color="transparent">
          <v-hover>
            <v-img
              slot-scope="{ hover }"
              :src="client.src"
              :alt="client.name+' logo'"
              lazy-src="https://cdn.dribbble.com/users/503653/screenshots/3143656/fluid-loader.gif"
              height="100"
              width="160"
              aspect-ratio="2.75"
              contain
            >
              <v-expand-transition>
                <div
                  v-if="!hover"
                  class="transition-fast-in-fast-out blue v-img--reveal"
                  style="height: 100%;"
                ></div>
              </v-expand-transition>
            </v-img>
          </v-hover>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  metaInfo: {
    title: "Services",
    titleTemplate: "%s ← Eldin's Space",
    meta: [
      { name: "viewport", content: "width=device-width, initial-scale=1" },
      {
        name: "description",
        content:
          "Sulai's Services Web Development Front-End Technical Writing and Editorial Services"
      },
      { charset: "utf-8" },
      { property: "og:title", content: "Sulai Sivadel" },
      { property: "og:site_name", content: "Sulai Sivadel" },
      { property: "og:type", content: "website" },
      { property: "og:url", content: "https://www.sulai.me" },
      {
        property: "og:image",
        content: ""
      },
      {
        property: "og:description",
        content:
          "Sulai Sivadel's Services Web Development Front-End Design and Development Writing and Editiorial"
      }
    ]
  },
  data() {
    return {
      clients: [
        {
          name: "Party Dash",
          src: "https://i.imgur.com/5uBCmox.pngully/portfolio10/images/Smiley_Face_Logo.png",
          href: "https://partydash.com/",
          title: "Party Dash",
        },
        {
          name: "Mayapple Center for the Arts and Humanities",
          src: "https://i.imgur.com/6GR6DC5.jpg",
          href: "https://www.mayapplecenter.org/"
        },
        {
          name: "John David West",
          src: "https://i.imgur.com/cv4WrDO.jpg",
          href: "https://www.johndavidwest.com/"
        },
        {
          name: "Michelle Slater, PhD.",
          src:
            "https://i.imgur.com/TSWhSC3.jpg",
          href: "https://michelleslater.com/"
        },
      ],
      services: [
        {
          src: "https://i.imgur.com/GvTt5GG.png",
          title: "Web Development"
        },
        {
          src: "https://i.imgur.com/g74mGuU.png",
          title: "Web Design"
        },

        {
          src: "https://i.imgur.com/HIgAoGm.png",
          title: "Professional Writing/Editing"
        },
        {
          src: "https://i.imgur.com/FaCKzOC.png",
          title: "Technical Writing"
        }
      ]
    };
  }
};
</script>
<style >
.v-img--reveal {
  opacity: 0.3;
}
</style>