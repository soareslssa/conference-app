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
  <div id="event-cover" class="d-flex flex-column h-25 align-center pa-16">
    <h1 class="text-h4 text-xs-h6 text font-height-thin ">{{eventTitle}}</h1>
    <v-icon icon="fa-solid fa-calendar"></v-icon>
  </div>
</template>
<script>
import { defineComponent } from "@vue/composition-api";

export default defineComponent({
  setup() {

    return {
      eventTitle: 'WE MAKE BETTER DAYS l CARNIVAL EDITION 2024'
    }
  },
});
</script>
