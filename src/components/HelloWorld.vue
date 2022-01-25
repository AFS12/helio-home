<template>
  <v-container style="margin-top: 20px">
    <p style="font-weight: 300; color: #080e3d">Templates</p>
    <v-container style="background-color: #fcfcfc">
      <v-card elevation="0" dark class="rounded-xl gradient">
        <v-card-title primary-title class="justify-center">
          O que você gostaria de criar?
        </v-card-title>
        <v-card-text class="text-center">
          <v-row justify="center">
            <v-col md="2" xl="1">
              <v-btn class="rounded-xl" height="50px" color="#FFFFFF5C">
                <div
                  style="border: 2px solid #4b63dc; width: 22px; height: 30px"
                ></div>
              </v-btn>
              <br />
              <br />
              Cartaz
            </v-col>
            <v-col md="2" xl="1">
              <v-btn class="rounded-xl" height="50px" color="#FFFFFF5C">
                <div
                  style="border: 2px solid #4b63dc; width: 30px; height: 16px"
                ></div>
              </v-btn>
              <br />
              <br />
              Etiqueta
            </v-col>
            <v-col md="2" xl="1">
              <v-btn class="rounded-xl" height="50px" color="#FFFFFF5C">
                <div
                  style="border: 2px solid #4b63dc; width: 25px; height: 25px"
                ></div>
              </v-btn>
              <br />
              <br />
              RD Quadrada
            </v-col>
            <v-col md="2" xl="1">
              <v-btn class="rounded-xl" height="50px" color="#FFFFFF5C">
                <div
                  style="border: 2px solid #4b63dc; width: 14px; height: 23px"
                ></div>
              </v-btn>
              <br />
              <br />
              RD Stories
            </v-col>
            <v-col md="2" xl="1">
              <v-btn class="rounded-xl" height="50px" color="#FFFFFF5C">
                <div
                  style="border: 2px solid #4b63dc; width: 32px; height: 23px"
                ></div>
              </v-btn>
              <br />
              <br />
              TV
            </v-col>
          </v-row>
        </v-card-text>
      </v-card>
      <br />
      <v-text-field
        placeholder="O que você deseja?"
        dense
        background-color="white"
        append-icon="mdi-magnify"
        light
        filled
        rounded
      ></v-text-field>
      <br />
      <h3>Trabalhados Recentementes</h3>
      <br />
      <v-row>
        <v-col md="2">
          <v-img
            src="https://image.freepik.com/vetores-gratis/cardapio-de-comida-para-uso-digital-ilustrado_52683-45627.jpg"
            width="120"
            height="120"
            class="rounded-lg"
          ></v-img>
          <br />
          <br />
          Horti-fruti
          <br />
          <small>Há 4 dias</small>
        </v-col>
        <v-col md="2">
          <v-img
            src="https://image.freepik.com/vetores-gratis/cardapio-de-comida-para-uso-digital-ilustrado_52683-45627.jpg"
            width="120"
            height="120"
            class="rounded-lg"
          ></v-img>
          <br />
          <br />
          Horti-fruti
          <br />
          <small>Há 4 dias</small>
        </v-col>
        <v-col md="2">
          <v-img
            src="https://image.freepik.com/vetores-gratis/cardapio-de-comida-para-uso-digital-ilustrado_52683-45627.jpg"
            width="120"
            height="120"
            class="rounded-lg"
          ></v-img>
          <br />
          <br />
          Horti-fruti
          <br />
          <small>Há 4 dias</small>
        </v-col>
      </v-row>
      <br />
      <h3>Todos</h3>
      <br />
      <v-row>
        <v-col md="2">
          <v-img
            src="https://images-americanas.b2w.io/produtos/01/00/item/111063/7/111063733_1GG.jpg"
            width="150"
            height="210"
            class="rounded-lg"
          ></v-img>
          <br />
          <br />
          Horti-fruti
          <br />
          <small>Há 4 dias</small>
        </v-col>
        <v-col md="2">
          <v-img
            src="https://www.adobe.com/br/express/create/cover/media_19a7c3bcd464c0a9a955b9a538fe32f888e89c7e1.png?width=400&format=png&optimize=medium"
            width="150"
            height="210"
            class="rounded-lg"
          ></v-img>
          <br />
          <br />
          Horti-fruti
          <br />
          <small>Há 4 dias</small>
        </v-col>
        <v-col md="2">
          <v-img
            src="https://www.printgraf.net.br/uploads/produtos/winder-banner-tecido-sublimacao-16123843201910567800601b0840ba4f3.jpg"
            width="150"
            height="210"
            class="rounded-lg"
          ></v-img>
          <br />
          <br />
          Horti-fruti
          <br />
          <small>Há 4 dias</small>
        </v-col>
        <v-col md="2">
          <v-img
            src="data:image/jpeg;base64,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"
            width="150"
            height="210"
            class="rounded-lg"
          ></v-img>
          <br />
          <br />
          Horti-fruti
          <br />
          <small>Há 4 dias</small>
        </v-col>
        <v-col md="2">
          <v-img
            src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQIDGG-ZHHxdlEWHljMJej6oshKtTWWnfRQtw&usqp=CAU"
            width="150"
            height="210"
            class="rounded-lg"
          ></v-img>
          <br />
          <br />
          Horti-fruti
          <br />
          <small>Há 4 dias</small>
        </v-col>
      </v-row>
    </v-container>
  </v-container>
</template>

<script>
export default {
  name: "HelloWorld",

  data: () => ({
    ecosystem: [
      {
        text: "vuetify-loader",
        href: "https://github.com/vuetifyjs/vuetify-loader",
      },
      {
        text: "github",
        href: "https://github.com/vuetifyjs/vuetify",
      },
      {
        text: "awesome-vuetify",
        href: "https://github.com/vuetifyjs/awesome-vuetify",
      },
    ],
    importantLinks: [
      {
        text: "Documentation",
        href: "https://vuetifyjs.com",
      },
      {
        text: "Chat",
        href: "https://community.vuetifyjs.com",
      },
      {
        text: "Made with Vuetify",
        href: "https://madewithvuejs.com/vuetify",
      },
      {
        text: "Twitter",
        href: "https://twitter.com/vuetifyjs",
      },
      {
        text: "Articles",
        href: "https://medium.com/vuetify",
      },
    ],
    whatsNext: [
      {
        text: "Explore components",
        href: "https://vuetifyjs.com/components/api-explorer",
      },
      {
        text: "Select a layout",
        href: "https://vuetifyjs.com/getting-started/pre-made-layouts",
      },
      {
        text: "Frequently Asked Questions",
        href: "https://vuetifyjs.com/getting-started/frequently-asked-questions",
      },
    ],
  }),
};
</script>

<style>
.gradient {
  background: #3a1c71;
  background: -webkit-linear-gradient(to top right, #4c61db, #26a8e0);
  background: linear-gradient(to top right, #4c61db, #26a8e0);
}
</style>