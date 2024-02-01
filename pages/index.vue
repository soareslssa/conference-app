<template>
  <div class="d-flex h-50">
    <v-parallax src="https://cdn.vuetifyjs.com/images/parallax/material.jpg">
      <div
        class="d-flex flex-column fill-height justify-center align-center text-white"
      >
        <h1 class="text-h4 font-weight-thin mb-4">Conference</h1>
        <h4 class="subheading">Conference description</h4>
      </div>
    </v-parallax>
  </div>

  <div
    class="d-flex justify-center align-center h-25"
  >
    <v-card elevation="0">
      <v-card-title class="text-h4 text-xs-h6 font-weight-black">
        {{ event.title }}
      </v-card-title>
      <v-card-text>
        <div class="my-2">
          <v-icon icon="fa-solid fa-calendar" />
          {{ event.startDate + ` > ` + event.endDate }}
        </div>
        <div class="my-2">
          <v-icon icon="fa-solid fa-location-dot"/>
          {{  event.location }}
        </div>
      </v-card-text>
    </v-card>
  </div>
</template>
<script>
import { defineComponent } from "@vue/composition-api";

export default defineComponent({
  setup() {
    return {
      event: {
        title: "WE MAKE BETTER DAYS l CARNIVAL EDITION 2024",
        startDate: "2024-02-09",
        endDate: "2024-02-12",
        location: "Evento presencial em Igreja Unidade em Cristo, Rio de Janeiro - RJ"
      },
    };
  },
});
</script>
