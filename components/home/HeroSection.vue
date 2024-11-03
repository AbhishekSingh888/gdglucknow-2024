<template>
  <v-container fluid class="px-md-15 py-md-8 pa-3 ">
    <v-row no-gutters class="d-flex align-center" justify="space-between">
      <v-col cols="12" md="5" class="d-flex align-center justify-center py-4">
        <div class="content-wrapper">
          <h2 class="mb-4 text-center text-md-left">{{ mainData.welcome.title }} <span class="border bg-white px-3" style="border-radius:50px">2024</span></h2>
          <p class="description text-center text-md-left">
            {{ mainData.eventInfo.description.long }}
          </p>

          <p class="my-5 d-flex align-center justify-center justify-md-start">
            <v-icon class="mr-2">mdi-calendar-blank</v-icon>
            {{ mainData.eventInfo.date }}
          </p>

          <div class="d-flex justify-center justify-md-start">
            <v-btn rounded size="large" color="#FFD427" to="/events" class="my-4 mt-3" target="_blank"
              style="border: 1.5px solid #1e1e1e; color: black; text-transform: capitalize; font-weight: 600; font-size: 16px;"
              variant="flat">
              Book Your Pass Now
              <v-icon class="ml-2">mdi-ticket-confirmation</v-icon>
            </v-btn>
          </div>
        </div>
      </v-col>

      <v-col cols="12" md="6" class="d-flex align-center justify-center" style="position: relative;">
        <div class="shadow-box mobile-none" style="position: absolute; top: 14px; right: 14px; background-color: #ccf6c5;
           border: 1px solid #504e4e;
          width: 100%; height: 100%;">
        </div>

        <div class="image-wrapper" style="position: relative; z-index: 1;">
          <v-img alt="GDG Logo" src="assets/img/sticker.png" lazy-src="assets/img/gdglogo.svg" class="logo-image"
            contain></v-img>
        </div>
      </v-col>
    </v-row>





    <v-row justify-center align="center" class="desktop-none">
      <v-col md="12" sm="12" cols="12">
        <v-img alt="logo" src="assets/img/gdgarrow.svg" lazy-src="assets/img/gdgarrow.svg"></v-img>
        <v-img alt="logo" src="assets/img/gdglogo.svg" lazy-src="assets/img/gdglogo.svg" style="width: 50%;"></v-img>
        <div class="d-flex">
          <v-img alt="logo" src="assets/img/Vector.svg" lazy-src="assets/img/Vector.svg" style="width: 10%;"></v-img>
          <div>
            <h1 class="responsive-h1 my-4 pt-4">
              <!-- <span style="font-size: 170%;color:#19154A">DevFest</span><br /> -->
              <v-img alt="logo" src="assets/img/devfesttext.svg" lazy-src="assets/img/devfesttext.svg"></v-img>
              <span style="display: block;padding-top: 10px; font-weight: 500;">{{ mainData.communityLocation.city }}
                2024</span>
            </h1>
          </div>
          <v-img alt="logo" src="assets/img/Vectorright.svg" lazy-src="assets/img/Vectorright.svg"
            style="width: 10%;"></v-img>
        </div>

        <div class="space-wrapper ">
          <p class="" :style="{ maxWidth: '100%' }">
            {{ mainData.eventInfo.description.short }}
          </p>

          <p class="my-5">
            <span class="mr-4">
              <v-icon class="mr-1">mdi-calendar-blank</v-icon>
              {{ mainData.eventInfo.date }}
            </span>
          </p>

          <v-btn rounded size="small" color="#FFD427" v-if="
            mainData.eventInfo &&
            mainData.eventInfo.registeration.link.length &&
            new Date(mainData.eventInfo.registeration.end_date) > new Date()
          " :href="mainData.eventInfo.registeration.link" class="my-4 mt-3" target="_blank"
            style="border: 1.5px solid #1e1e1e; color: #19154A;text-transform: capitalize;font-weight:600;width: 100%;font-size: 16px !important;letter-spacing: 0;"
            variant="flat">Find a DevFest near you</v-btn>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup>
import { useDisplay } from "vuetify";
const { width, mobile } = useDisplay();
const screenWidth = ref(width);
const { mainData } = useJSONData();
</script>

<style scoped>
.image-wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  padding: 3rem;
  border: 1px solid #504e4e;
  background-color: white;
}

.logo-image {
  width: 100%;
  height: auto;
  max-width: 400px;
}


@media (max-width: 960px) {

  .content-wrapper,
  .image-wrapper {
    max-width: 90%;
    padding: 1rem;
  }
}

.responsive-h1 {
  font-size: 250%;
  line-height: 100%;
}

.vectorimg {
  width: 25%;

}

.gdglogo {
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.desktop-none {
  display: none;
}

.mobile-none {
  display: flex;
}

.space-wrapper {
  padding-top: 60px !important;
  padding-bottom: 40px !important;
}

/* Media query for screens larger than 600px */
@media (min-width: 600px) {
  .responsive-h1 {
    font-size: 300%;
  }
}

@media (max-width: 668px) {
  .desktop-none {
    display: flex;
  }

  .mobile-none {
    display: none;
  }

  .space-wrapper {
    padding-top: 40px !important;
  }
}
</style>
