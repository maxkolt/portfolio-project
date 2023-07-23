<template>
  <v-app-bar app color="black" dark flat class="px-12" style="">
    <v-btn
        icon="fa-solid fa-bars"
        color="yellow"
        @click="toggleNav"
        class="burger-btn"
        v-if="isMobile">
    </v-btn>

    <v-spacer v-if="isMobile"></v-spacer>

    <v-btn @click="scroll('home')">
      <v-icon color="yellow" left class="mr-2">fas fa-signature</v-icon>
      <h3>M.K</h3>
    </v-btn>

    <v-spacer v-if="isMobile"></v-spacer>

    <v-row class="nav-links" v-if="!isMobile">
      <v-spacer></v-spacer>
      <v-btn text @click="scroll('home')" class="text-yellow">Главная</v-btn>
      <v-btn text @click="scroll('about')">Обо мне</v-btn>
      <v-btn text @click="scroll('portfolio')">Портфолио</v-btn>
      <v-btn text @click="scroll('contact')">Контакты</v-btn>
    </v-row>
    <DarkMode/>
  </v-app-bar>
  <v-menu
      class="mt-15 justify-center"
      v-if="isMobile"
      bottom left
      v-model="menuOpen"
      style="position: fixed"
  >
    <template v-slot:activator="{ on }">
      <v-btn icon v-on="on" class="burger-btn"></v-btn>
    </template>
    <v-list style="background-color: black">
      <v-list-item v-for="(item, i) in navigationItems" :key="i" @click="selectMenuItem(item.ref)">
        <v-list-item-title style="color: white">{{ item.title }}</v-list-item-title>
      </v-list-item>
    </v-list>
  </v-menu>
</template>

<script>
import DarkMode from "./DarkMode.vue";

export default {
  components: {DarkMode},
  data() {
    return {
      isMobile: false,
      navigationItems: [
        {title: "Главная", ref: "home"},
        {title: "Обо мне", ref: "about"},
        {title: "Портфолио", ref: "portfolio"},
        {title: "Контакты", ref: "contact"},
      ],
      menuOpen: false,
    };
  },
  methods: {
    scroll(refName) {
      const element = document.getElementById(refName);
      element.scrollIntoView({behavior: "smooth"});
      this.menuOpen = false;
    },
    toggleNav() {
      this.menuOpen = !this.menuOpen;
    },
    selectMenuItem(refName) {
      this.scroll(refName);
    },
  },
  mounted() {
    this.isMobile = window.innerWidth <= 600;
  },
};
</script>

<style scoped>
@media (max-width: 600px) {

  .nav-links {
    display: none;
  }

  .burger-btn {
    display: block;
  }

  .burger-btn {
    margin-left: 8px;
  }
}
</style>
