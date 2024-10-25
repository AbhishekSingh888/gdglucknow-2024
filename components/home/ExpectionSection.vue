<template>
  <v-container fluid style="margin-bottom: 6%;">
    <v-row>
      <v-col md="12" sm="12">
        <h1>What to Expect</h1>
        <p>
          Get ready for the most anticipated annual event hosted by Google Developers Group Lucknow! DevFest Lucknow is all about bringing technology closer to developers like you. Join us for an immersive all-day developer conference where we'll dive deep into a multitude of cutting-edge technologies through lightning talks, insightful sessions, hands-on workshops, and more.
        </p>
      </v-col>
      <v-col
        md="4"
        sm="4"
        cols="12"
        v-for="(item, index) in mainData.eventInfo.whatToExpect"
        :key="index"
      >
        <div
        :style="{ backgroundColor: item.color || '#eeeeee' }"
          style="
            border-radius: 40px;
            border: 1.5px solid black;
          "
        >
          <v-img
            :src="getImage(index + 1)"
            width="50"
            alt="image"
            class="float-right mr-5 pt-8"
          ></v-img>
          <div class="pa-8">
            <h2>{{ item.title }}</h2>
            <p style="font-size: 95%">
              {{ item.description }}
            </p>
          </div>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup>
import img1 from "@/assets/img/section-elements/expect1.svg";
import img2 from "@/assets/img/section-elements/expect2.svg";
import img3 from "@/assets/img/section-elements/expect3.svg";

const { mainData } = useJSONData();
const getImage = (index) => {
  if (index == 1) return img1;
  if (index == 2) return img2;
  if (index == 3) return img3;
  if (index == 4) return img3;
  if (index == 5) return img2;
  if (index == 6) return img1;
};
</script>

<style>
</style>
