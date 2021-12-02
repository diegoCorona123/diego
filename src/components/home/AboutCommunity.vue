<template>
  <v-container fluid class="pa-0">
    <v-row align="center" class>
      <v-col cols="12" md="12" lg="12" sm="12" class="pa-0" style="color:white">
        <div class="ma-1">
          <div class="pa-5">
            <p class="google-font mb-0" style="font-size:150%">#Automatización</p>
            <p
              class="google-font mt-0"
              style="font-size:95%"
            >la tecnología que permite a cualquier persona configurar un software o también llamado “robot” para simular y desarrollar las acciones de un “humano” que interactúa dentro de sistemas digitales para ejecutar diferentes procesos de negocios,
            son sistemas diseñados para realizar determinadas tareas, por lo general repetitivas y regladas eliminando de dicha tarea al empleado.</p>
            <v-btn
              v-if="checkExistance(config.generalConfig.meetupLink,0)"
              :href="config.generalConfig.meetupLink"
              target="_blank"
              outlined
              color
              class="ma-0 google-font mb-2"
              style="border-radius:5px;text-transform: capitalize;color:white"
            >Inscribete</v-btn>&nbsp;
            <br />
            <router-link
              to="/about"
              class="google-font"
              style="text-decoration:none;color:white"
            >Comunicacaion {{config.generalConfig.shortName || config.generalConfig.name}}</router-link>
          </div>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import { mapState } from "vuex";

export default {
  name: "App",
  data: () => ({}),
  computed: {
    ...mapState(["config"])
  }
};
</script>