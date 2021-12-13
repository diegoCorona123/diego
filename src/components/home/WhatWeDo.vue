<template>
  <v-container fluid>
    <v-row align="center" justify="center">
      <v-col cols="12" md="3" lg="3" sm="4" class>
        <p class="google-font mb-0" style="font-size:150%">NOTA</p>
        <p
          class="google-font mt-0"
          style="font-size:95%"
        >Bienbenido a un nuevo mundo lleno de evolucion sobre la nueva tecnologuia #ROBOT</p>
        <p class="google-font" style="font-size:95%">TODAS LAS TECNOLOGIAS</p>
        <span v-for="(item,i) in whatwedodata" :key="i">
          <v-tooltip bottom>
            <template v-slot:activator="{ on }">
              <a :href="item.link" target="_blank" class="ma-0 mx-3" rel="noreferrer">
                <img :src="getImgUrl(item.image)" width="25vh" alt srcset dark v-on="on" />
              </a>
              &nbsp;&nbsp;&nbsp;
            </template>
            <span>{{item.TechName}}</span>
          </v-tooltip>
        </span>
      </v-col>
      <v-col cols="12" md="9" lg="9" sm="8">
        <v-container fluid>
          <v-row>
            <v-col md="3" lg="3" sm="6" cols="6" class="text-center pa-2">
              <v-icon large style="font-size:300%">mdi-robot</v-icon>
              <p class="google-font mt-2" style="font-size:130%">robotica</p>
              <p
                class="google-font"
                style="font-size:95%"
              >La mejor enseñansa para todos y para todas en todo su campo.</p>
            </v-col>
            <v-col md="3" lg="3" sm="6" cols="6" class="text-center pa-2">
              <v-icon large style="font-size:300%">mdi-code-tags</v-icon>
              <p class="google-font mt-2" style="font-size:130%">Programacion</p>
              <p
                class="google-font"
                style="font-size:95%"
              >Los lenguajes mas utizados y mejor explicados faciles de entenders.</p>
            </v-col>
            <v-col md="3" lg="3" sm="6" cols="6" class="text-center pa-2">
              <v-icon large style="font-size:300%">mdi-school</v-icon>
              <p class="google-font mt-2" style="font-size:130%">Preparacion</p>
              <p
                class="google-font"
                style="font-size:95%"
              >Te preparamos para que tengas los mejores conocimientos en tu campo.</p>
            </v-col>
            <v-col md="3" lg="3" sm="6" cols="6" class="text-center pa-2">
              <v-icon large style="font-size:300%">mdi-android</v-icon>
              <p class="google-font mt-2" style="font-size:130%">Programas</p>
              <p
                class="google-font"
                style="font-size:95%"
              >Los mejores programas con las mejores herramientas listas para su funcionamiento</p>
            </v-col>
          </v-row>
        </v-container>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import whatwedodata from "@/assets/data/whatwedo.json";
export default {
  name: "App",
  data: () => ({
    whatwedodata: whatwedodata
  }),
  methods: {
    getImgUrl(url) {
      if (url.length > 0) {
        return require("@/assets/img/what-we-do/" + url);
      } else {
        return require("@/assets/img/what-we-do/notFound.png");
      }
    }
  }
};
</script>