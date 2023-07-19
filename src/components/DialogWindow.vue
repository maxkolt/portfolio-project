<template>
  <div class="text-center">
    <v-dialog
        v-model="dialog"
        width="auto"
    >
      <template v-slot:activator="{ props }">
        <v-btn
            class="mt-15"
            color="#FBDF7E"
            v-bind="props"
        >
          Напиши мне
        </v-btn>
      </template>

      <v-card>
        <v-card-text>
          <v-btn
              icon="fas fa-phone-alt"
              class="mp-4"
          >
          </v-btn>
          +7 925-59611-51<br/><br/>
          <v-btn
              icon="fas fa-envelope"
              class="mp-4"
          >
          </v-btn>
          12345kolt@gmail.com
        </v-card-text>
        <v-card-actions>
          <v-btn variant="tonal" block @click="dialog = false">Закрыть</v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </div>
</template>

<script>
export default {
  data() {
    return {
      dialog: false,
    }
  },
}
</script>