<template>
  <div class="d-flex h-25">
    <v-parallax :src="event.cover">
      <div
        class="d-flex flex-column fill-height justify-center align-center text-white"
      >
        <h1 class="text-h4 font-weight-thin mb-4">Conference</h1>
        <h4 class="subheading">Conference description</h4>
      </div>
    </v-parallax>
  </div>
  <v-container class="pa-4">
    <v-row>
      <v-col cols="2" class="d-none d-md-flex"></v-col>
      <v-col>
        <section name="header" class="align-md-center flex-md-column ga-3">
          <v-chip class="my-4" color="primary">
            <i class="fa-regular fa-credit-card mr-2"></i>
            Parcele sua compra em até 12x</v-chip
          >
          <div class="d-flex flex-column text-center text-md-left ga-6">
            <div class="text-h5 text-md-h4 font-weight-black">
              {{ event.title }}
            </div>
            <div>
              <i class="fa-regular fa-calendar mr-2"></i>
              {{ event.startDate + ` > ` + event.endDate }}
            </div>
            <div>
              <i class="fa-solid fa-location-dot mr-2"></i>
              Evento presencial em
              <a :href="event.link">{{ event.location }} </a>
            </div>
          </div>
        </section>

        <section name="description" class="align-md-center flex-md-column">
          <div class="d-flex flex-column align-md-center">
            <div class="justify-center align-center">
              <div class="text-h5 font-weight-black my-4">
                Descrição do evento
              </div>
              <div>{{ event.description }}</div>
            </div>
          </div>
        </section>
      </v-col>
      <v-col cols="2" class="d-none d-md-flex"></v-col>
    </v-row>
  </v-container>
</template>
<script>
import { defineComponent } from "@vue/composition-api";

export default defineComponent({
  setup() {
    return {
      event: {
        title: "WE MAKE BETTER DAYS l CARNIVAL EDITION 2024",
        cover:
          "https://images.unsplash.com/photo-1604177052603-c2b4cff228db?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D",
        startDate: "2024-02-09",
        endDate: "2024-02-12",
        location: "Igreja Unidade em Cristo, Rio de Janeiro - RJ",
        link: "http://www.instagram.com/unidadeemcristooficial",
        description:
          "Bem-vindos, homens de de Deus, ao primeiro culto especial com o tema 'Mover'. Nos reuniremos para juntos caminharmos a jornada de movimento em nossas vidas. Como homens, somos chamados a avançar, superar desafios e crescer em todas as áreas. Neste momento importantíssimo para nosas vidas, refletiremos sobre a coragem que nos impulsiona, a resiliência que nos move adiante e a fé que nos guia em cada passo. Que este culto inspire ação, desperte o propósito e fortaleça os laços  que nos unem como seguidores comprometidos da caminhada com Deus. Esperamos por você e te desafiamos a convidar outro homem para estar conosco. A entrada é franca, mas pedimos que traga 1Kg de alimento não perecível para ajudarmos famílias assitidas pela nossa Ação Social.",
      },
    };
  },
});
</script>
