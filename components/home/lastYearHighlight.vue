<template>
  <v-container fluid>
    <v-row class="mb-0">
      <v-col md="12" sm="12" cols="12">
        <h1 class="section-title">What last year's highlights</h1>
        <p class="section-description">
          DevFest 2023 was a remarkable event that brought together over 1,000 enthusiastic attendees and more than 35
          industry experts for an exciting day of learning and inspiration. Participants immersed themselves in 25+
          engaging sessions, including lightning talks, hands-on workshops, and discussions focused on the latest
          innovations in technology. The event highlighted the strength of community and collaboration, offering
          valuable insights into emerging trends and tools in the tech world.
        </p>
      </v-col>
    </v-row>
    <v-row>
      <v-col md="4" sm="6" cols="12" v-for="(image, index) in images" :key="index">
        <v-img
          :src="image"
          class="mb-4 styled-image"
          :style="{ '--delay': `${index * 100}ms` }"
          aspect-ratio="1.75"
        >
        </v-img>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup>
import { ref } from 'vue';
const { mainData } = useJSONData();
const colors = ref(["#C3ECF6", "#F8D8D8", "#FFE7A5", "#CCF6C5"]);
import img1 from "@/assets/img/glimps/IMG_0257.png";
import img2 from "@/assets/img/glimps/IMG_0216.png";
import img3 from "@/assets/img/glimps/IMG_0377.png";

const images = ref([img1, img2, img3,img1, img2, img3]);
</script>

<style scoped>

.styled-image {
  animation: slideInText 0.5s ease-in-out;
  animation-fill-mode: forwards;
  opacity: 0;
  border: 1.5px solid black;
  box-shadow: -8px 8px 0px 0px #ccf6c5;  
  transition: box-shadow 0.3s ease-in-out; 
}

.styled-image:hover {
  box-shadow: -10px 10px 0px 0px #34a853;
}

.styled-image:nth-child(odd) {
  animation-delay: var(--delay);
}

.styled-image:nth-child(even) {
  animation-delay: var(--delay);
}

@keyframes slideInText {
  from {
    opacity: 0;
    transform: translateX(100%);
  }
  to {
    opacity: 1;
    transform: translateX(0);
  }
}
</style>