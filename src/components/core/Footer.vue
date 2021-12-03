<template>
  <v-footer
    height="auto"
    fixedfir
    class="hidden-sm-and-down ma-0"
    :class="this.$vuetify.theme.dark == true?'grey darken-4':'white'"
  >
  <!-- style="border-color:#e0e0e0;border-width: 1px;border-style: solid;border-bottom: 0;border-left:0;border-right:0" -->
    <v-container fluid >
      <v-row align="center" justify="center" class="my-0 py-0">
        <v-col cols="12" md="10" lg="10" sm="11" class="py-0 my-0">
          <v-divider v-if="!this.$vuetify.theme.dark"></v-divider>
          <!-- {{socialLinks}} -->
          <CommunitySocialInfo :config="config"/>
          <v-divider></v-divider>
        </v-col>
      </v-row>

      <v-row align="center" justify="center" class="mt-3">
        <v-col cols="12" md="10" lg="10" sm="11" class="my-0 py-0">
          <v-container fluid class="pa-0 my-0">
            <!-- Links Section -->

            <v-row justify="start" class="">
              <v-col cols="12" md="3" lg="3" sm="3" class="py-2" >
                  <p class="google-font mb-0" style="font-size: 140%;font-weight: 300;"><b>Create Dc ♣</b></p>
                  
              </v-col>

              <v-col cols="12" md="3" lg="3" sm="3" class="py-2" >
                  <p class="google-font mb-0" style="font-size: 140%;font-weight: 300;"><b>Ubicacion:Dubai</b></p>
                  
              </v-col>

              <v-col cols="12" md="3" lg="3" sm="3" class="py-2" >
                  <p class="google-font mb-0" style="font-size: 140%;font-weight: 300;"><b>Telefono:099</b></p>
              </v-col>
            </v-row>

            <!-- Links Section -->
          </v-container>
        </v-col>
      </v-row>

      <v-row align="center" justify="center" class="mb-0">
        <v-col cols="12" md="10" lg="10" sm="11" class="px-0 mx-0"> 
          <v-divider></v-divider>
          <v-toolbar text class="pa-0 px-0 mt-3 mx-0 elevation-0" style="padding:0 !important" :class="this.$vuetify.theme.dark == true?'grey darken-4':'white'">
            <v-toolbar-title class="google-font pl-0 ml-0 mr-3" style="font-size:200%">RPA[Automatización robótica]</v-toolbar-title>
            
               
            <v-spacer></v-spacer>
           <span >Project 
          <a
            
          > WEB</a></span>
          </v-toolbar>
        </v-col>
      </v-row>

    </v-container>
  </v-footer>
</template>

<script>
import { mapState } from 'vuex'
  export default {
    components:{
      CommunitySocialInfo : ()=>import('@/components/common/CommunitySocialInfo'),
    },
    data:()=>({
    }),
    computed:{
      ...mapState(['config'])
    },
  }
</script>

<style scoped>
  .darkThemeTextLink{
    color: #FAFAFA
  }
  .lightThemeTextLink{
    color: #3E4551
  }
</style>