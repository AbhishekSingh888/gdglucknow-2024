<template>
    <h1 class="text-center">Choose Your Dev Fest 2024 Experience</h1>
    <p class="text-center">Explore ticket options and secure your spot at the year's biggest developer event!</p>
    
    <v-container class="d-flex justify-center pa-10 mt-10">
      <v-row align="stretch" >
        <!-- Early Bird Ticket -->
        <v-col cols="12" md="4" class="d-flex" >
          <div class="shadow-wrapper">
            <v-card class="pricing-card early-bird-card flex-column" outlined>
              <v-card-title class="title">Early Bird Ticket</v-card-title>
              <v-card-subtitle class="price">₹99</v-card-subtitle>
              <v-card-text class="flex-grow-1">
                <p class="subtext">Available until Jan 31, 2024</p>
                <div class="divider"></div>
                <p>Gain full access to all sessions and workshops at Dev Fest 2024 with an early bird discount.</p>
              </v-card-text>
              <v-card-actions>
                <v-btn class="neumorphic-btn mt-auto">Register Now</v-btn>
              </v-card-actions>
            </v-card>
          </div>
        </v-col>
  
        <!-- Standard Ticket -->
        <v-col cols="12" md="4" class="d-flex">
          <div class="shadow-wrapper">
            <v-card class="pricing-card standard-card flex-column" outlined>
              <v-card-title class="title">Standard Ticket</v-card-title>
              <v-card-subtitle class="price">₹149</v-card-subtitle>
              <v-card-text class="flex-grow-1">
                <p>Access to all sessions and workshops, conference swag, and networking events.</p>
                <div class="divider"></div>
                <p>Join us at Dev Fest 2024 and connect with industry leaders.</p>
              </v-card-text>
              <v-card-actions>
                <v-btn class="neumorphic-btn mt-auto">Register Now</v-btn>
              </v-card-actions>
            </v-card>
          </div>
        </v-col>
  
        <!-- VIP Ticket -->
        <v-col cols="12" md="4" class="d-flex">
          <div class="shadow-wrapper">
            <v-card class="pricing-card vip-card flex-column" outlined>
              <v-card-title class="title">VIP Ticket</v-card-title>
              <v-card-subtitle class="price">₹299</v-card-subtitle>
              <v-card-text class="flex-grow-1">
                <p>All benefits of the Standard Ticket plus exclusive VIP lounge access, reserved seating, and post-conference dinner event.</p>
                <div class="divider"></div>
                <p><strong>Experience Dev Fest 2024 like a VIP!</strong></p>
              </v-card-text>
              <v-card-actions>
                <v-btn class="neumorphic-btn mt-auto">Register Now</v-btn>
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

.neumorphic-btn:hover {
  background: #ffe7a5;
  box-shadow: -3px 3px 0px 0 #000;
  cursor: pointer;
}

.mt-auto {
  margin-top: auto;
}

.standard-card{
    background-color: #ffe7a5;
}
</style>
