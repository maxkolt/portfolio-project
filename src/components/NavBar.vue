<template>
  <v-app-bar app color="black" dark flat class="px-12">
    <v-btn>
      <v-icon color="yellow" left class="mr-2">fas fa-signature</v-icon>
      <h3>M.K</h3>
    </v-btn>

    <v-spacer></v-spacer>
    <v-btn text @click="scroll('home')" class="text-yellow">Главная</v-btn>
    <v-btn text @click="scroll('about')">Обо мне</v-btn>
    <v-btn text @click="scroll('portfolio')">Портфолио</v-btn>
    <v-btn text @click="scroll('contact')">Контакты</v-btn>
  </v-app-bar>
</template>

<script>
export default {
  methods: {
    scroll(refName) {
      const element = document.getElementById(refName);
      element.scrollIntoView({behavior: "smooth"});
    },
  },
}

</script>

<style scoped>

</style>