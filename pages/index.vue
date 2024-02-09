<template>
  <div class="d-flex h-25">
    <v-parallax :src="event.image">
      <div
        class="d-flex flex-column fill-height justify-center align-center text-white"
      >
        <h1 class="text-h4 font-weight-thin mb-4">Conference</h1>
        <h4 class="subheading">Conference description</h4>
      </div>
    </v-parallax>
  </div>

  <v-container class="d-flex flex-column pa-4 ga-6">
    <section>
      <v-chip
        class="my-4"
        color="primary"
        prepend-icon="fa-regular fa-credit-card"
        text="Parcele sua compra em até 12x"
      />
      <div class="d-flex flex-column text-center text-md-left ga-6">
        <div class="text-h5 text-md-h4 font-weight-black">
          {{ event.name }}
        </div>
        <div>
          <i class="fa-regular fa-calendar mr-2"></i>
          {{ event.start_date + ` > ` + event.end_date }}
        </div>
        <div>
          <i class="fa-solid fa-location-dot mr-2"></i>
          {{ event.category_sec.name }}
          <a :href="event.url">{{ event.address.name }} </a>
        </div>
      </div>
    </section>

    <section>
      <div class="d-flex flex-column ga-4">
        <div class="text-h5 font-weight-black">Descrição do evento</div>
        <div>{{ event.detail }}</div>
      </div>
    </section>
  </v-container>
</template>
<script>
import { defineComponent } from "@vue/composition-api";
import axios from "axios";

export default defineComponent({
  setup() {
    let event = {}
    return {
      event,
    };
  },
  methods: {
    getEvent() {
      axios
        .get("https://api.sympla.com.br/public/v4/events/2338147", {
          headers: {
            s_token:
              "65669bee0503134c00d6f9ba6f6223df1f6f4b07244781d7ccc7211ce50b822f",
          },
        })
        .then((response) => {
          let r = response.data
          this.event = r.data
          console.log(this.event)
        });
    },
  },
  mounted() {
    this.getEvent();
  },
});
</script>
<style scoped>
.v-container {
  max-width: 75rem;
}
</style>
