<template>
  <v-app>
    <v-app-bar
      app
      elevation="0"
      color="#FCFCFC"
      style="justify-content: center"
    >
      <v-row style="margin-top: 15px" justify="space-between">
        <v-col md="1" @click="drawer = !drawer">
          <v-btn icon>
            <v-icon color="#26A8E0">mdi-menu</v-icon>
          </v-btn>
        </v-col>
        <v-col md="4">
          <v-text-field
            placeholder="O que você deseja?"
            dense
            background-color="white"
            append-icon="mdi-magnify"
            light
            filled
            rounded
          ></v-text-field>
        </v-col>
        <v-col md="2">
          <v-btn
            class="btn btn-block"
            rounded
            elevation="0"
            color="#E6E9FF"
            large
          >
            <h5 class="barBtnPrint">
              <v-icon color="#2D9BE0">mdi-printer-outline</v-icon>
              Ver fila de impressão
            </h5>
          </v-btn>
        </v-col>
        <v-col md="1"></v-col>
        <v-col md="4">
          <v-row justify="end">
            <v-col md="5">
              <v-btn
                class="btn btn-block"
                rounded
                elevation="0"
                color="#4E5CDB"
                large
              >
                <h5 class="barBtnNew">
                  <v-icon color="white">mdi-plus</v-icon>
                  criar novo
                </h5>
              </v-btn>
            </v-col>
            <v-col md="2">
              <v-btn fab small elevation="0" color="#E6E9FF">
                <v-badge overlap dot bordered offset-x="9" color="#F14976">
                  <v-icon color="#080E3D">mdi-bell-outline</v-icon>
                </v-badge>
              </v-btn>
            </v-col>
            <v-col md="2">
              <v-avatar size="40">
                <img src="https://github.com/AFS12.png" />
              </v-avatar>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-app-bar>
    <v-navigation-drawer app v-model="drawer" color="#4E5CDB" dark>
      <v-list-item two-line centered>
        <v-list-item-content>
          <v-row>
            <v-spacer></v-spacer>
            <v-col>
              <v-img
                src="https://byprice.com.br/wp-content/uploads/2017/05/logotipo-byprice-primario.png"
                max-width="150"
              ></v-img>
            </v-col>
            <v-spacer></v-spacer>
          </v-row>
          <v-row>
            <v-col>
              <v-select
                :items="selectItems"
                rounded
                v-model="defaultSelected"
                background-color="white"
                light
                filled
              ></v-select>
            </v-col>
          </v-row>
        </v-list-item-content>
      </v-list-item>

      <v-list>
        <v-list-item-group active-class="selected">
          <v-list-item
            style="font-weight: 300"
            v-for="item in items"
            :key="item.title"
            @click="menuIndex(item.index)"
          >
            <v-list-item-icon>
              <v-icon>{{ item.icon }}</v-icon>
            </v-list-item-icon>

            <v-list-item-content>
              <v-list-item-title>{{ item.title }}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <div :style="menuBarStyle"></div>
        </v-list-item-group>
      </v-list>
      <v-list>
        <v-row>
          <v-spacer></v-spacer>
          <v-col>
            <v-btn text> Ajuda </v-btn>
          </v-col>
          <v-spacer></v-spacer>
        </v-row>
      </v-list>
    </v-navigation-drawer>

    <v-main>
      <HelloWorld />
    </v-main>
  </v-app>
</template>

<script>
import HelloWorld from "./components/HelloWorld";

export default {
  name: "App",

  components: {
    HelloWorld,
  },

  data: () => ({
    items: [
      { title: "Dashboard", icon: "mdi-view-dashboard-outline", index: 0 },
      { title: "Templates", icon: "mdi-book-open-variant", index: 1 },
      { title: "Campanhas", icon: "mdi-purse-outline", index: 2 },
      { title: "Arte Avulsa", icon: "mdi-tag-outline", index: 3 },
      { title: "Fila de Impressão", icon: "mdi-printer-outline", index: 4 },
      { title: "Download", icon: "mdi-cloud-download-outline", index: 5 },
    ],
    selectItems: [
      "Loja - Água Verde",
      "Loja - Água Verde 2",
      "Loja - Água Verde 3",
      "Loja - Água Verde 4",
    ],
    defaultSelected: "Loja - Água Verde",
    drawer: true,
    menuBarStyle: {
      width: "4px",
      height: "48px",
      backgroundColor: "#35D9A4",
      position: "relative",
      left: "5px",
      top: "-332px",
      display: "flex",
    },
  }),
  methods: {
    menuIndex(index) {
      const moveValue = 56;
      const baseValue = -332;
      let finalValue = moveValue * index + baseValue;
      this.menuBarStyle.top = `${finalValue}` + "px";
    },
  },
};
</script>

<style>
.selected {
  color: #080e3d !important;
}

.teste {
  width: 4px;
  height: 48px;
  background-color: #35d9a4;
  position: relative;
  left: 5px;
  top: -332px;
  display: flex;
}

.barBtnPrint {
  color: #2b9edf;
  font-size: 10px;
  font-weight: 400;
}
.barBtnNew {
  color: white;
  font-size: 10px;
  font-weight: 400;
}
</style>