<template>
  <v-dialog v-model="dialog" width="800">
    <template v-slot:activator="{ on }">
      <div
        v-on="on"
        v-ripple
        style="cursor: pointer;"
        :class="$vuetify.theme.dark == true?'darkModeCardFeatureEvent':'lightModeCardFeatureEvent'"
        class="pa-3 py-5 fill-height"
      >
        <p class="google-font mb-0" style="font-size:90%">{{data.date | dateFilter}}</p>
        <p>ROS</p>
        <p>Cursos Monterrey</p>
        <v-spacer></v-spacer>
        <p class="mb-0 mt-2 google-font" style="color:#1a73e8">INFORMACION</p>
      </div>
    </template>
    
    <v-card
      color
      v-if="dialog"
      class
      style="border-radius:5px"
      :class="this.$vuetify.theme.dark == true?'grey darken-3':'white'"
    >
      <v-card-title class="px-5 py-5 google-font" style="background-position:right bottom;">
        <p>ROS</p>
        <v-spacer></v-spacer>
        <v-tooltip bottom>
      <template v-slot:activator="{ on }">
        <v-btn icon v-on="on" :href="'events/'+data.id" target="_blank">
          <v-icon>mdi-open-in-new</v-icon>
        </v-btn> 
      </template>
      <span>Abrir en una pestaña nueva</span>
    </v-tooltip>
        
      </v-card-title>

      <v-card-text class="pb-5 pt-0">
        <p class="google-font mb-0" style="font-size:120%">{{data.date}}</p>
        <p>Abierto</p>
        <p class="google-font">{{data.time.starttime}} - {{data.time.endtime}}</p>

        <p class="google-font mb-0" style="font-size:95%">
          <b>Cursos monterrey</b>
        </p>
        <p>
ROS significa Robot Operating System. Es un marco de código abierto que se utiliza para ayudar en el desarrollo de robots avanzados.
En esta capacitación en vivo dirigida por un instructor, los participantes aprenderán cómo comenzar a usar ROS para sus proyectos de robótica a través del uso de herramientas de visualización y simulación de robótica.</p>

        

        <v-btn
          color="#1a73e8"
          v-if="checkExistance(data.links.registration,0)"
          href="https://www.nobleprog.mx/ros/cursos/monterrey"
          target="_blank"
          class="ma-0 elevation-0 my-2 mr-3"
          dark
          style="text-transform: capitalize;"
        >Mas Informacion</v-btn>
        <v-btn
          color="pink"
          v-if="checkExistance(data.links.meetup,0)"
          href="https://www.google.com/maps/search/Boulevard+D%C3%ADaz+Ordaz+140,+,+Monterrey,+NLE,+64650,+mx/@25.6718403,-100.3900869,15z/data=!3m1!4b1"
          target="_blank"
          class="ma-0 elevation-0 my-2 mr-3"
          dark
          style="text-transform: capitalize;"
        >Visitanos</v-btn>
      
      </v-card-text>

      <v-divider></v-divider>

      <v-card-actions :class="this.$vuetify.theme.dark == true?'grey darken-3':'grey lighten-3'">
        <v-spacer></v-spacer>
        <v-btn color="primary" text @click="dialog = false">Exit</v-btn>
      </v-card-actions>
    </v-card>
  </v-dialog>
</template>

<script>
export default {
  props: ["data"],
  data() {
    return {
      dialog: false
    };
  },
  methods: {
    goToEvent(id) {
      this.$router.push("/events/" + id);
    }
  },
  filters: {
    summary: (val, num) => {
      if (val.length > num) {
        return val.substring(0, num) + "..";
      } else {
        return val;
      }
    },
    dateFilter: value => {
      const date = new Date(value);
      return date.toLocaleString(["en-US"], {
        month: "short",
        day: "2-digit",
        year: "numeric"
      });
    }
  }
};
</script>

<style scoped>
.lightModeCardFeatureEvent {
  background-color: #ffff;
  box-shadow: 0 0 36px rgba(0, 0, 0, 0.1);

  border-radius: 8px;
}
.darkModeCardFeatureEvent {
  background-color: #292929;
  box-shadow: 0 0 36px rgba(0, 0, 0, 0.1);
  /* border:1px solid #212121; */
  border: 1px solid #424242;
  border-radius: 5px;
}
</style>