<template>
  <v-container fluid>
    <v-row justify="space-between" align="center" class="main-row pa-5">
      <v-col md="5" sm="6" cols="12" class="text-left">
        <h1 class="keep-in-touch-text">
          Keep in touch with {{ mainData.communityName }} for the latest
          announcements
        </h1>
        <p class="mb-3 stake-out">
          Stake out #{{ mainData.communityName }} for the latest updates and news.
        </p>
        <CommonSpeakerSocialButton :socialLinks="mainData.communityLinks" />
      </v-col>

      <v-col md="3" sm="5" cols="12">
        <v-img class="gdg-logo" alt="logo" src="/assets/img/gdg.png"></v-img>
        <h1 class="devfest-title">DevFest</h1>
        <h2 class="devfest-year">Lucknow'24</h2>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup>
const { mainData } = useJSONData();
import CommonSpeakerSocialButton from '@/components/common/speakerSocialButton.vue';
</script>

<style>
.main-row {
  background-color: #FFE7A5;
  border-radius: 20px;
  border: 2px solid black;
}

.keep-in-touch-text {
  color: rgba(25, 21, 74, 1);
  line-height: normal;
  margin: 0;
}

.stake-out {
  color: rgba(25, 21, 74, 1);
}

.devfest-title,
.devfest-year {
  margin: 0;
}

.devfest-title {
  font-size: 55px;
  font-weight: 900;
  line-height: 76.8px;
  color: #19154A;
}

.devfest-year {
  font-size: 53px;
  font-weight: 900;
  line-height: 74.4px;
  color: rgba(253, 214, 99, 1);
  text-shadow: -3px 3px black;
  -webkit-text-stroke: 0.1px rgba(25, 21, 74, 1);
}

.gdg-logo {
  width: 125px;
  height: 68px;
  border-radius: 12px 0px 0px 0px;
  margin-bottom: 20px;
}

.text-left {
  text-align: left;
}

.text-right {
  text-align: right;
}
</style>
