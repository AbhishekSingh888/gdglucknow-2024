<template>
    <v-container class="d-flex justify-center pa-10">
      <v-row class="pricing-cards" justify="center">
        <v-col cols="12" md="4" class="mb-5">
          <PricingCard
            :title="'STANDARD LOGO DESIGN'"
            :price="'$500'"
            :features="[
              '1 logo variation',
              '4 revisions',
              'Color palette',
              'All .pdf .svg .png delivery',
              'Est. 7 days of delivery',
            ]"
            buttonText="Click here to get started"
            :highlight="false"
          />
        </v-col>
        <v-col cols="12" md="4" class="mb-5">
          <PricingCard
            :title="'PROFESSIONAL LOGO DESIGN'"
            :price="'$899'"
            :features="[
              '2 logo variations',
              '10 revisions',
              'Color palette',
              'All .pdf .svg .png delivery',
              'Est. 7 days of delivery',
            ]"
            buttonText="Click here to get started"
            :highlight="true"
          />
        </v-col>
        <v-col cols="12" md="4" class="mb-5">
          <PricingCard
            :title="'PREMIUM LOGO DESIGN'"
            :price="'$1499'"
            :features="[
              '3 logo variations',
              'Unlimited revisions',
              'Color palette',
              'All .pdf .svg .png delivery',
              'Est. 7 days of delivery',
            ]"
            buttonText="Click here to get started"
            :highlight="false"
          />
        </v-col>
      </v-row>
    </v-container>
  </template>
  
  <script>
  import PricingCard from "@/components/pricing/pricingcard.vue";
  
  export default {
    components: {
      PricingCard,
    },
  };
  </script>
  
  <style scoped>
  .pricing-cards {
    gap: 20px;
  }
  </style>
  