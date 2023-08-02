<template>
  <v-app>
    <router-link to="/other-app" class="bottom-left-link">
      <img :src="imagePath" style="height: 60px; cursor:pointer" alt="img">
    </router-link>
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
  },
  data() {
    return {
      imagePath: 'few clouds.png'
    }
  }
}

</script>

<style>
body {
  margin: 0;
  font-family: "Roboto-Condensed-Light", "ui-sans-serif";
}

.bottom-left-link {
  z-index: 9999;
  position: fixed;
  bottom: 20px;
  left: 15px;
}


</style>

