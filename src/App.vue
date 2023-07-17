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