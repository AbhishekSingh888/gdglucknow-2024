<template>
  <h1 class="text-center">Choose Your Dev Fest 2024 Pass</h1>
  <p class="text-center">Grab your pass early to enjoy discounted rates and be part of the biggest developer gathering of the year!</p>
  
  <v-container class="d-flex justify-center pa-10 mt-10">
    <v-row align="stretch">
      <!-- Early Bird Pass -->
      <v-col cols="12" md="4" class="d-flex">
        <div class="shadow-wrapper">
          <v-card class="pricing-card early-bird-card flex-column" outlined>
            <v-card-title class="title">Early Bird Pass</v-card-title>
            <v-card-subtitle class="price">₹299</v-card-subtitle>
            <v-card-text class="flex-grow-1">
              <p class="subtext">Available: Announced Soon</p>
              <div class="divider"></div>
              <p>Get full access to all Dev Fest 2024 sessions, workshops, and networking opportunities at a special early rate!</p>
            </v-card-text>
            <v-card-actions>
              <v-btn class="neumorphic-btn mt-auto" disabled>Register Soon</v-btn>
            </v-card-actions>
          </v-card>
        </div>
      </v-col>

      <!-- Standard Pass -->
      <v-col cols="12" md="4" class="d-flex">
        <div class="shadow-wrapper">
          <v-card class="pricing-card standard-card flex-column" outlined>
            <v-card-title class="title">Standard Pass</v-card-title>
            <v-card-subtitle class="price">₹349</v-card-subtitle>
            <v-card-text class="flex-grow-1">
              <p class="subtext">Available: Announced Soon</p>
              <div class="divider"></div>
              <p>Access all sessions, workshops, networking events, and conference swag! Join us to connect and learn from industry leaders.</p>
            </v-card-text>
            <v-card-actions>
              <v-btn class="neumorphic-btn mt-auto" disabled>Register Soon</v-btn>
            </v-card-actions>
          </v-card>
        </div>
      </v-col>

      <!-- Last-Minute Pass -->
      <v-col cols="12" md="4" class="d-flex">
        <div class="shadow-wrapper">
          <v-card class="pricing-card last-minute-card flex-column" outlined>
            <v-card-title class="title">Last-Minute Pass</v-card-title>
            <v-card-subtitle class="price">₹499</v-card-subtitle>
            <v-card-text class="flex-grow-1">
              <p class="subtext">Available: Announced Soon</p>
              <div class="divider"></div>
              <p>Get the same great access to all events, sessions, and workshops! Don’t miss out on the biggest developer event of the year.</p>
            </v-card-text>
            <v-card-actions>
              <v-btn class="neumorphic-btn mt-auto" disabled>Register Soon</v-btn>
            </v-card-actions>
          </v-card>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
name: "PricingPlans",
};
</script>

<style scoped>
.pricing-card {
  cursor: pointer;
  text-align: center;
  min-height: 26rem;
  padding: 16px;
  display: flex;
  flex-direction: column;
  border: 1px solid #000;
  background-color: #ffffff;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.shadow-wrapper {
display: flex;
flex-direction: column;
width: 100%;
padding: 8px;
border: 1px solid #000;
box-shadow: 15px 15px 30px rgba(0, 0, 0, 0.2), -15px -15px 30px rgba(255, 255, 255, 0.8);
transition: box-shadow 0.3s ease, transform 0.3s ease;
}

.shadow-wrapper:hover {
transform: translateY(-10px);
box-shadow: -10px 10px 0px rgba(0, 0, 0, 1), -10px -10px 20px rgba(255, 255, 255, 0);
}

.title {
font-weight: bold;
font-size: 18px;
}

.price {
font-size: 4rem;
font-weight: bold;
color: #f9ab00;
opacity: 1;
text-shadow: 2px 2px 0px rgba(0, 0, 0, 0.9);
}

.subtext {
color: #666;
}

.divider {
margin: 8px 0;
border-bottom: 1px solid #000;
}

.neumorphic-btn {
display: inline-flex;
justify-content: center;
align-items: center;
padding: 12px 24px;
font-weight: bold;
border-radius: 0%;
border: 1px solid #000;
color: #333;
background: #f9ab00;
transition: background 0.2s ease, box-shadow 0.2s ease;
}

.neumorphic-btn[disabled] {
background: #cccccc;
cursor: not-allowed;
box-shadow: none;
}

.mt-auto {
margin-top: auto;
}

.standard-card {
  background-color: #ffe7a5;
}
</style>
