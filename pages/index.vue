<template>
  <div class="d-flex h-50">
    <v-parallax :src="event.cover">
      <div
        class="d-flex flex-column fill-height justify-center align-center text-white"
      >
        <h1 class="text-h4 font-weight-thin mb-4">Conference</h1>
        <h4 class="subheading">Conference description</h4>
      </div>
    </v-parallax>
  </div>

  <div class="d-flex justify-center align-center h-25">
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
          <v-icon icon="fa-solid fa-location-dot" />
          {{ event.location }}
        </div>
      </v-card-text>
    </v-card>
  </div>
  <div class="d-flex justify-center flex-column w-25">
    <div class="text-h5 font-weight-black my-4">Descrição do evento</div>
    <div> {{  event.description }}</div>
  </div>
</template>
<script>
import { defineComponent } from "@vue/composition-api";

export default defineComponent({
  setup() {
    return {
      event: {
        title: "WE MAKE BETTER DAYS l CARNIVAL EDITION 2024",
        cover: "https://images.unsplash.com/photo-1604177052603-c2b4cff228db?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D",
        startDate: "2024-02-09",
        endDate: "2024-02-12",
        location:
          "Evento presencial em Igreja Unidade em Cristo, Rio de Janeiro - RJ",
        description:
          "Bem-vindos, homens de de Deus, ao primeiro culto especial com o tema 'Mover'. Nos reuniremos para juntos caminharmos a jornada de movimento em nossas vidas. Como homens, somos chamados a avançar, superar desafios e crescer em todas as áreas. Neste momento importantíssimo para nosas vidas, refletiremos sobre a coragem que nos impulsiona, a resiliência que nos move adiante e a fé que nos guia em cada passo. Que este culto inspire ação, desperte o propósito e fortaleça os laços  que nos unem como seguidores comprometidos da caminhada com Deus. Esperamos por você e te desafiamos a convidar outro homem para estar conosco. A entrada é franca, mas pedimos que traga 1Kg de alimento não perecível para ajudarmos famílias assitidas pela nossa Ação Social.",
      },
    };
  },
});
</script>
