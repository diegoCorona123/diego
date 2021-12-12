<template>
  <p class="google-font mt-4 mb-3" style="font-size:130%">
    Contactanos:
    <v-tooltip top v-if="checkExistance(config.generalConfig.socialLinks.facebook,0)">
      <template v-slot:activator="{ on }">
        <v-btn
          text
          icon
          v-on="on"
          rel="noreferrer"
          href="https://www.facebook.com/KUKAGlobal/"
          target="_blank"
          slot="activator"
        >
          <v-icon>mdi-facebook</v-icon>
        </v-btn>
      </template>
      <span>Facebook</span>
    </v-tooltip>
    <v-tooltip top v-if="checkExistance(config.generalConfig.socialLinks.youtube,0)">
      <template v-slot:activator="{ on }">
        <v-btn
          text
          icon
          v-on="on"
          rel="noreferrer"
          href="https://www.youtube.com/c/KukaRobotGroup"
          target="_blank"
          slot="activator"
        >
        
          <v-icon>mdi-youtube-play</v-icon>
        </v-btn>
      </template>
      <span>YouTube</span>
    </v-tooltip>
    
  </p>
</template>

<script>
export default {
  name: "CommunitySocialInfo",
  props: ["config"],
};
</script>

<style>
</style>