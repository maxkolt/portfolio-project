<template>
  <v-app id="home">
    <NavBar/>
    <v-container fluid>
      <div class="head">
        <v-row>
          <v-col cols="5">
            <div style="position: relative" class="mt-16">
              <h1 class="text-grey">Привет!</h1>
              <h2 class="text-white">Меня зовут Максим Колтович</h2>
              <span class="text-grey">Я frontend-разработчик</span><br/>
              <v-btn tile dark class="text-yellow mt-8" variant="outlined">
                Связаться
              </v-btn>
            </div>
          </v-col>
          <v-col cols="2">
            <div
                style="
                position: absolute;
                z-index: 9999;
                bottom: 0;
                margin-left: auto;
                margin-right: auto;
                left: 0;
                right: 0;
                text-align: center;"
                class="mt-16">
              <v-icon>fas fa-angle-double-down</v-icon>
            </div>
          </v-col>
          <v-col cols="5">
            <div style="position: relative; z-index: 9999" class="mt-16">
              <v-img src="raboti.png" contain max-height="300"></v-img>
            </div>
          </v-col>
        </v-row>
      </div>
      <v-col cols="12" class="mt-16" id="about">
        <div>
          <v-row>
            <v-col cols="12" sm="6">
              <div class="egg">
                <v-img class=mt-20 src="bookcod.png" max-height="250"></v-img>
              </div>
            </v-col>
            <v-col cols="12" sm="6">
              <h2 class="mt-16">Обо мне</h2>
              <div style="width: 120px">
                <v-slider
                    v-model="slider2"
                    color="yellow"
                    label="track-color"
                ></v-slider>
              </div>
              <h4 class="mt-n4">Я креативный веб-дизайнер</h4>
              <h4 class="">И разработчик</h4>
              <p class="text-grey">
                Я опытный frontend-разработчик с фокусом на создании впечатляющих и интуитивно понятных веб-приложений.
                Имея более чем трех лет опыта в этой области, я обладаю глубокими знаниями HTML, CSS и JavaScript, а
                также
                опытом работы с современными фреймворками и библиотеками, такими как Vue.js и TypeScript. Моими сильными
                сторонами являются внимательность к деталям, способность работать в команде и
                стремление к постоянному самосовершенствованию. Я ищу возможность применить свои навыки и креативность в
                динамичной команде разработчиков.
              </p>
              <br/>
              <p class="text-grey">
                Я стремлюсь к разработке веб-приложений, которые обеспечивают отличный пользовательский опыт и являются
                функциональными и масштабируемыми. Мой подход к разработке включает использование передовых технологий,
                лучших практик и аккуратного кодирования. Я умею эффективно взаимодействовать с дизайнерами и
                бэкэнд-разработчиками, чтобы обеспечить гармоничную интеграцию фронтенда с остальной частью проекта.
                Кроме
                того, я открыт к изучению новых технологий и готов к постоянному профессиональному росту. Если вы ищете
                опытного frontend-разработчика, который может привнести инновации и качество в вашу команду, я готов
                взяться за новые вызовы.
              </p>
              <v-btn tile dark color="yellow" class="mt-4">
                Скачать резюме
              </v-btn>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <div class="text-center mt-4">
        <h2>что я делаю</h2>
        <div style="width: 120px; margin: 0 auto">
          <v-slider
              v-model="slider2"
              color="yellow"
              label="track-color"
          ></v-slider>
        </div>
      </div>
      <v-col cols="12" class="padd" id="portfolio">
        <div class="first" id="project">
          <v-row>
            <v-col cols="12">
              <div class="child">
                <v-btn
                    icon="fas fa-laptop"
                    color="#FBDF7E"
                    class="text-white"
                ></v-btn>
                <h3 class="ml-3 mt-4">Веб-дизайн</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  Lorem, ipsum dolor sit amet <br/>consectetur adipisicing
                  <br/>consectetur adipis
                </p>
              </div>
              <div class="child">
                <v-btn
                    icon="fas fa-mobile-alt"
                    color="#FBDF7E"
                    class="text-white"
                ></v-btn>
                <h3 class="ml-3 mt-4">Разработка</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  Lorem, ipsum dolor sit amet <br/>consectetur adipisicing
                  <br/>consectetur adipis
                </p>
              </div>
              <div class="child">
                <v-btn
                    icon="fas fa-code"
                    color="#FBDF7E"
                    class="text-white"
                ></v-btn>
                <h3 class="ml-3 mt-4">Кодинг</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  Lorem, ipsum dolor sit amet <br/>consectetur adipisicing
                  <br/>consectetur adipis
                </p>
              </div>
            </v-col>
          </v-row>
          <v-divider></v-divider>
        </div>
      </v-col>
    </v-container>
  </v-app>
</template>

<script>
import {defineComponent} from 'vue'
import HelloWorld from './components/HelloWorld.vue'
import NavBar from "./components/NavBar.vue";

export default defineComponent({
  name: 'App',

  components: {
    NavBar,
    HelloWorld,
  },

})
</script>
<style scoped>
.v-container {
  padding: 16px 0 16px 0;
}

.head {
  position: relative;
  text-align: center;
  padding: 12px;
  margin-bottom: 6px;
  height: 400px;
  width: 100%;
  color: white;
}

.head:before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 50%;
  background: black;
  transform: skew(0deg, 6deg);
}

.head:after {
  content: "";
  position: absolute;
  top: 0;
  right: 0;
  height: 100%;
  width: 50%;
  background: black;
  transform: skew(0deg, -6deg);
}

.egg {
  display: block;
  margin-left: 100px;
  margin-top: 70px;
  width: 356px;
  height: 300px;
  background-color: #fbdf7e;
  border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
}

.first {
  width: 100%;
  height: 280px;
  text-align: center;
  padding: 2rem 2rem;
}

.child {
  display: inline-block;
  padding: 2rem 5rem;
  vertical-align: middle;
  text-align: center;
  margin-right: 8px;
}
.img{
  margin-top: 20px;
}
</style>
