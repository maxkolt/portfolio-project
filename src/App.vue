<template>
  <v-app>
    <NavBar/>
    <BodyView/>
  </v-app>
</template>

<script>
import BodyView from "./components/BodyView.vue";
import NavBar from "./components/NavBar.vue";

export default {
  name: 'App',
  components: {
    NavBar,
    BodyView
  }
}
</script>

<style>
body {
  margin: 0;
  font-family: "Roboto-Condensed-Light", "ui-sans-serif";
}
</style>

