<template>
  <v-app class="icon ml-4">
    <v-icon
        style="color: #626060"
        class="custom-icon"
        icon="fa-solid fa-circle-half-stroke"
        @click="toggleTheme"
    >
    </v-icon>
  </v-app>
</template>

<script>
import {useTheme} from 'vuetify'

export default {
  setup() {
    const theme = useTheme()

    return {
      darkMode: false,
      theme,
      toggleTheme: () => theme.global.name.value = theme.global.current.value.dark ? 'light' : 'dark'
    }
  },
}
</script>
<style scoped>
.v-application {
  background: none;
}

.custom-icon {
  font-size: 32px;
  cursor: pointer;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
</style>