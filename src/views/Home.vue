<template>
  <v-layout column justify-center align-center class="mt-4 pt-2">
    <v-carousel hide-delimiters>
    <v-carousel-item
      v-for="(item,i) in items"
      :key="i"
      :src="item.src"
    ></v-carousel-item>
  </v-carousel>
    <vue-typer class="headline" :repeat="0" text="Sulai Sivadel"></vue-typer>
    <vue-typer
      :text="text1"
      :repeat="Infinity"
      :shuffle="false"
      initial-action="erasing"
      :pre-type-delay="70"
      :type-delay="70"
      :pre-erase-delay="1980"
      :erase-delay="150"
      erase-style="select-back"
      :erase-on-complete="false"
      caret-animation="smooth"
    ></vue-typer>
    <br>
    <v-flex xs12 sm6 md4 lg4 xl4 max-width="fluid">
      <v-card flat color="transparent">
        <v-card-title primary-title>
          <div style="background:#f5f5f7;color:#80bdf6">
            <h4 class="headline mb-0">
              <span></span>
                <div> 
                  <p>
                    Hello! I am Sulai Sivadel. I'm a Frontend Developer who
                   is passionate about
                   <span
                     class="blue--text font-weight-bold">
                   </span>building great user experiences.
                      I  am ambitious and user-focused with experience working in teams and independently. I have strong project management experience and experience delegating responsibilities to a team. <p>
                      A flexible and quick learner committed to constantly  learning and evolving skills to stay abreast of ever-evolving technologies and trends in the industry. Communicative, knowledgeable and steadfast with excellent computer engineering skills. HTML5, CSS,JavaScript, VueJS, and ReactJS.<p>When I'm not coding, you'll find me baking delicous desserts.</p>
                </div>
            </h4>
          </div>
        </v-card-title>

        <v-card-actions class="hidden-sm-and-down">
          <v-btn
            v-for="icon in icons"
            :key="icon.icon"
            fab
            dark
            outline
            color="blue"
            :href="icon.href"
            target="_blank"
          >
            <v-icon dark>{{icon.icon}}</v-icon>
          </v-btn>
        </v-card-actions>

        <v-card-actions class="hidden-md-and-up justify-center">
          <v-btn
            v-for="icon in icons"
            :key="icon.icon"
            small
            fab
            dark
            outline
            color="blue"
            :href="icon.href"
            target="_blank"
          >
            <v-icon dark>{{icon.icon}}</v-icon>
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
import { VueTyper } from "vue-typer";
import VueCompareImage from "vue-compare-image";

export default {
  metaInfo: {
    title: "Home",
    titleTemplate: "%s ← Sulai Sivadel",
    meta: [
      { name: "viewport", content: "width=device-width, initial-scale=1" },
      { name: "description", content: "Sulai Sivadel's Portfolio" },
      { charset: "utf-8" },
      { property: "og:title", content: "" },
      { property: "og:site_name", content: "Sulai's World" },
      { property: "og:type", content: "website" },
      { property: "og:url", content: "https://www.sulai.me" },
      {
        property: "og:image",
        content: "https://i.imgur.com/Dcz2PGx.jpg"
      },
      { property: "og:description", content: "Sulai's Portfolio" }
    ]
  },
  components: {
    "vue-typer": VueTyper,
    VueCompareImage
  },
  data() {
    return {
      icons: [
        { href: "https://github.com/sulai3030", icon: "fab fa-github" },
        {
          href: "https://stackoverflow.com/users/9226831/sulai3030",
          icon: "fab fa-stack-overflow"
        },
        { href: "https://https://twitter.com/Sulai2020", icon: "fab fa-twitter" },
        {
          href: "https://www.https://www.linkedin.com/in/sulai3030",
          icon: "fab fa-linkedin-in"
        },
      ],
      text1: ["Front-End Developer", "Web Developer", "Web Designer"],
      sliderLine: 0,
      hSize: 0,
      sliderPosition: 0.5,
        items: [
          {
            src: 'https://i.imgur.com/pKAfYqJ.jpg',
          },
          {
            src: 'https://i.imgur.com/sZVpwww.jpg',
          },
          {
            src: 'https://i.imgur.com/yqk5uxS.jpg',
          },
          {
            src: 'https://i.imgur.com/OjfJyq9.jpg?1',
          },
        ],
    };
  },
};
</script>
<style>
@keyframes rocking {
  0%,
  100% {
    transform: rotateZ(-10deg);
  }

  50% {
    transform: rotateZ(10deg);
  }
}

.vue-typer {
  font-family: Arial, "Helvetica Neue", Helvetica, sans-serif;
}
.vue-typer .custom.char.typed {
  color: blue;
}
.vue-typer .custom.char.selected {
  color: #e91e63;
}

.vue-typer .custom.caret {
  animation: rocking 1s ease-in-out 0s infinite;
}
.vue-typer .custom.caret.typing {
  background-color: blue;
}
.vue-typer .custom.caret.selecting {
  display: inline-block;
  background-color: #e91e63;
}
</style>

