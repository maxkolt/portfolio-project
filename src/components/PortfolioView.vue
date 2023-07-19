<template>
  <v-col cols="12" sm="12" mt="16" class="mt-16" id="services">
    <div class="d-flex justify-center mb-6">
      <v-btn class="mr-2" color="#FBDF7E" @click="showAll">Все</v-btn>
      <v-btn class="mr-2" variant="tonal" @click="showDiplomas">Дипломы</v-btn>
      <v-btn class="mr-2" variant="tonal" @click="showCertificates">Сертификаты</v-btn>
    </div>
  </v-col>

  <v-col cols="12" class="imgHover">
    <v-row class="fill-height" align="center" justify="center">
      <template v-for="(item, i) in filteredItems" :key="i">
        <v-col cols="12" md="4">
          <v-hover v-slot="{ isHovering, props }">
            <v-card
                :elevation="isHovering ? 12 : 2"
                :class="{ 'on-hover': isHovering }"
                v-bind="props"
            >
              <v-img :src="item.img" height="225px"></v-img>
            </v-card>
          </v-hover>
        </v-col>
      </template>
    </v-row>
  </v-col>
</template>

<script>
export default {
  name: "PortfolioView",
  data() {
    return {
      items: [
        {img: "diplom1.jpeg"},
        {img: "diplom2.jpeg"},
        {img: "diplom3.jpeg"},
        {img: "diplom6.jpeg"},
        {img: "diplom4.jpeg"},
        {img: "diplom5.jpeg"},
      ],
      filteredItems: [],
    };
  },
  methods: {
    showAll() {
      this.filteredItems = this.items;
    },
    showDiplomas() {
      this.filteredItems = this.items.slice(0, 3); // Выбираем первые 3 элемента для дипломов
    },
    showCertificates() {
      this.filteredItems = this.items.slice(3); // Выбираем последние 3 элемента для сертификатов
    },
  },
  created() {
    this.showAll(); // Показываем все фотографии изначально
  },
};
</script>


<style scoped>

.imgHover {
  padding: 0 100px;
}
</style>