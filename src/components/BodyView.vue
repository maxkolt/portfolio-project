<template>
  <v-app id="home">
    <v-container fluid>
      <div class="head">
        <v-row>
          <v-col cols="5">
            <div style="position: relative" class="mt-16">
              <h1 class="text-grey">Привет!</h1>
              <h2 class="text-white">Меня зовут Максим Колтович</h2>
              <span class="text-grey">Я frontend-разработчик</span><br/>
              <v-btn text @click="scroll('contact')" dark class="text-yellow btn-link mt-8" variant="outlined">
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
              <v-img class="mobile-styles" src="raboti.png" contain max-height="300"></v-img>
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
                    v-model="slider1"
                    color="yellow"
                ></v-slider>
              </div>
              <h3 class="mt-n4">Я креативный веб-дизайнер и разработчик</h3>
              <br/>
              <h4 class="text-grey">
                Имея более чем трех лет опыта в этой области, я обладаю глубокими знаниями HTML, CSS и JavaScript, а
                также
                опытом работы с современными фреймворками и библиотеками, такими как Vue.js и TypeScript. Моими сильными
                сторонами являются внимательность к деталям, способность работать в команде и
                стремление к постоянному самосовершенствованию. Я ищу возможность применить свои навыки и креативность в
                динамичной команде разработчиков.
              </h4>
              <br/>
              <h4 class="text-grey">
                Я стремлюсь к разработке веб-приложений, которые обеспечивают отличный пользовательский опыт и являются
                функциональными и масштабируемыми. Мой подход к разработке включает использование передовых технологий,
                лучших практик и аккуратного кодирования. Я умею эффективно взаимодействовать с дизайнерами и
                бэкэнд-разработчиками, чтобы обеспечить гармоничную интеграцию фронтенда с остальной частью проекта.
                Кроме
                того, я открыт к изучению новых технологий и готов к постоянному профессиональному росту. Если вы ищете
                опытного frontend-разработчика, который может привнести инновации и качество в вашу команду, я готов
                взяться за новые вызовы.
              </h4>
              <v-btn tile dark color="yellow" class="mt-4" @click="downloadResume">
                Скачать резюме
              </v-btn>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <div class="text-center mt-16">
        <h2>Стек</h2>
        <div style="width: 120px; margin: 0 auto">
          <v-slider
              v-model="slider2"
              color="yellow"
          ></v-slider>
        </div>
      </div>
      <v-col cols="12" class="padd" id="portfolio">
        <div class="first" id="project">
          <v-row>
            <v-col cols="12">
              <div class="child">
                <v-btn
                    icon="fa-brands fa-vuejs"
                    color="#FBDF7E"
                    class="text-white"
                ></v-btn>
                <h3 class="ml-3 mt-4">VUE</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  Гибкий, прогрессивный,<br/>компонентный язык
                </p>
              </div>
              <div class="child">
                <v-btn
                    icon="fas fa-code"
                    color="#FBDF7E"
                    class="text-white"
                ></v-btn>
                <h3 class="ml-3 mt-4">TypeScript</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  Типизированный,<br/> объектно-ориентированный
                </p>
              </div>
              <div class="child">
                <v-btn
                    icon="fa-brands fa-react"
                    color="#FBDF7E"
                    class="text-white"
                ></v-btn>
                <h3 class="ml-3 mt-4">React</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  Популярная, декларативная,<br/> компонентная библиотека
                </p>
              </div>
              <div class="child">
                <v-btn
                    icon="fa-brands fa-square-js"
                    color="#FBDF7E"
                    class="text-white"
                ></v-btn>
                <h3 class="ml-3 mt-4">JavaScript</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  Мощный, интерпретируемый
                  <br/> язык программирования
                </p>
              </div>
            </v-col>
          </v-row>
          <v-divider></v-divider>
        </div>
      </v-col>
      <PortfolioView/>
      <v-col class="text-center mt-16">
        <h2 class="mt-16">Мои проекты</h2>
        <div style="width: 120px; margin: 0 auto">
          <v-slider
              v-model="slider3"
              color="yellow"
          ></v-slider>
        </div>
      </v-col>
      <v-col cols="12" id="page">
        <div class="pre">
          <v-row>
            <v-col cols="12" sm="4" class="">
              <v-card class="mx-auto" max-width="344" height="" @click="openLinkOne">
                <v-img src="project1.jpg" height="200px" cover></v-img>
                <v-card-title>Проект MOVE-APP</v-card-title>
                <v-card-subtitle>
                  Реализован | 25 Авг 2021
                </v-card-subtitle>
                <v-card-text>
                  Удобное приложение для поиска, отслеживания, рекомендации и оценки фильмов.
                  Большой выбор современных киноновинок.
                </v-card-text>
              </v-card>
            </v-col>
            <v-col cols="12" sm="4">
              <v-card class="mx-auto" max-width="344" height="" @click="openLinkTwo">
                <v-img src="project3.jpg" height="200px" cover></v-img>
                <v-card-title>Проект YOUR-SHOP</v-card-title>
                <v-card-subtitle>
                  Реализован | 02 Фев 2023
                </v-card-subtitle>
                <v-card-text>
                  Онлайн-платформа, для удобной покупки товаров с сортировкой, добавление в
                  корзину и выборка по ценовой категории.
                </v-card-text>
              </v-card>
            </v-col>
            <v-col cols="12" sm="4">
              <v-card class="mx-auto" max-width="344" height="" @click="openLinkThree">
                <v-img src="project2.jpg" height="200px" cover></v-img>
                <v-card-title>Проект FURNITURE</v-card-title>
                <v-card-subtitle>
                  Реализован | 06 Сен 2022
                </v-card-subtitle>
                <v-card-text>
                  Проект магазин мебели, для комфортного и стильного обустройства интерьера.
                  Большой выбор мебели и фурнитуры.
                </v-card-text>
              </v-card>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <v-col class="mt-2" cols="12" id="biog">
        <div class="hire">
          <v-row>
            <v-col cols="12" sm="8">
              <h1 class="mt-9">Возьми меня в свою команду</h1>
              <p class="text-grey">
                Вместе мы будет создавть крутые проекты, вдохновляться новыми идеями и развивать IT индустрию
              </p>
            </v-col>
            <v-col cols="12" sm="4">
              <DialogWindow/>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <v-col cols="12" sm="12" class="px-16 mt-16" id="contact">
        <v-row>
          <v-col cols="12" sm="4">
            <div class="child">
              <h1>Контактная инфо.</h1>
              <v-btn
                  icon="fas fa-map-marker-alt"
                  color=""
                  class="mt-10"
                  variant="outlined"
                  @click="openMap"
              ></v-btn
              >
              <br/>
              <span class="text-caption">{{ address }}</span>
              <br/>
              <v-btn
                  icon="fas fa-phone-alt"
                  color=""
                  class="mt-10"
                  variant="outlined"
                  @click="makeCall"
              ></v-btn
              >
              <br/>
              <span class="text-caption">{{ phoneNumber }}</span> <br/>
              <span class="text-caption">8-916 1493356 </span> <br/>
              <v-btn
                  icon="fas fa-envelope"
                  color=""
                  class="mt-10"
                  variant="outlined"
                  @click="sendEmail"
              ></v-btn
              >
              <br/>
              <span class="text-caption">{{ email }}</span><br/>
              <span class="text-caption">kolt12max@mail.ru</span> <br/>
            </div>
          </v-col>
          <v-col cols="12" sm="8">
            <h1 class="mt-8">Отправить сообщение</h1>
            <v-divider></v-divider>
            <span class="text-caption"
            >Благодаря различным вариантам связи,
              вы можете выбрать наиболее удобный способ общения со мной.
              Я всегда рад помочь и ответить на ваши вопросы.
            </span
            >
            <v-row class="mt-10">
              <v-col cols="12" sm="6">
                <v-text-field
                    label="Ф.И.О"
                    persistent-hint
                    variant="outlined"
                ></v-text-field>
              </v-col>
              <v-col cols="12" sm="6">
                <v-text-field
                    label="Номер тел."
                    persistent-hint
                    variant="outlined"
                ></v-text-field>
              </v-col>
            </v-row>
            <v-textarea
                label="Сообщение"
                persistent-hint
                variant="outlined"
            ></v-textarea>
            <v-btn color="#FBDF7E" class="mt-2">Отправить</v-btn>
          </v-col>
        </v-row>
      </v-col>
    </v-container>
    <FooterView/>
  </v-app>
</template>

<script>
import {defineComponent} from "vue";
import FooterView from './FooterView.vue'
import PortfolioView from "./PortfolioView.vue";
import DialogWindow from "./DialogWindow.vue";

export default defineComponent({
  name: "BodyView",
  components: {FooterView, DialogWindow, PortfolioView},

  setup() {
    return {
      address: 'ул.Большая Академическая д47к1',
      phoneNumber: '8-925 5961151',
      email: '12345kolt@gmail.com',
      slider2: 50,
      slider1: 70,
      slider3: 100,
      tempName: '',
      tempPhoneNumber: '',
      tempMessage: '',
    }
  },

  methods: {
    scroll(refName) {
      const element = document.getElementById(refName);
      element.scrollIntoView({behavior: "smooth"});
    },
    downloadResume() {
      const resumeUrl = 'https://hh.ru/resume_converter/%D0%9A%D0%BE%D0%BB%D1%82%D0%BE%D0%B2%D0%B8%D1%87%20%D0%9C%D0%B0%D0%BA%D1%81%D0%B8%D0%BC%20%D0%A1%D0%B5%D1%80%D0%B3%D0%B5%D0%B5%D0%B2%D0%B8%D1%87.pdf?hash=7073f035ff0b574cd40039ed1f52695872526f&type=pdf&hhtmSource=resume&hhtmFrom=';
      const link = document.createElement('a');
      link.href = resumeUrl;
      link.download = 'resume.pdf';
      link.click();
    },
    sendEmail() {
      window.location.href = `mailto:${this.email}`;
    },
    makeCall() {
      window.location.href = `tel:${this.phoneNumber}`;
    },
    openMap() {
      const mapUrl = `https://www.google.com/maps/search/${encodeURIComponent(this.address)}`;
      window.open(mapUrl, '_blank');
    },
    openLinkOne() {
      window.open('https://github.com/maxkolt/movie-app', '_blank');
    },
    openLinkTwo() {
      window.open('https://github.com/maxkolt/your-shop', '_blank');
    },
    openLinkThree() {
      window.open('https://github.com/maxkolt/furnitureWebsiteOnJS', '_blank');
    }
  }
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
  margin-top: 170px;
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

.pre {
  width: 100%;
  text-align: center;
  padding: 0 200px;
  background-color: #f5f5f5;
}

.hire {
  width: 100%;
  height: 200px;
  padding: 0 200px;
  background-color: #e9e9e9;
  margin-top: -24px;
}

@media (max-width: 768px) {
  .head {
    padding: 0;
  }

  .egg {
    margin-left: auto;
    margin-right: auto;
    margin-top: 40px;
    width: 350px;
    height: 300px;
  }

  .btn-link {
    z-index: 9999;
    position: absolute;
    top: 100%;
    left: 87%;

  }

  .mobile-styles {
    margin-top: 150px;
    margin-left: -20px;
  }

  .first {
    display: contents;
  }

  .pre {
    display: contents;
  }

  .hire {
    display: contents;
  }

  .child {
    display: contents;
  }

  .mt-4 {
    margin-left: 0 !important;
  }
}

@media (min-width: 769px) and (max-width: 1024px) {
  .egg {
    margin-left: auto;
    margin-right: auto;
    margin-top: 200px;
    width: 300px;
    height: 300px;
  }
}

</style>
