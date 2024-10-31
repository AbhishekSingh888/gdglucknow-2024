<template>
    <v-card :class="['pricing-card', { 'highlight-card': highlight }]" elevation="3">
      <v-card-title class="title">{{ title }}</v-card-title>
      <v-card-subtitle class="price">{{ price }}</v-card-subtitle>
      <v-card-text>
        <ul class="features">
          <li v-for="(feature, index) in features" :key="index">{{ feature }}</li>
        </ul>
      </v-card-text>
      <v-card-actions>
        <v-btn class="start-btn" color="primary" outlined>{{ buttonText }}</v-btn>
      </v-card-actions>
    </v-card>
  </template>
  
  <script>
  export default {
    props: {
      title: String,
      price: String,
      features: Array,
      buttonText: String,
      highlight: Boolean,
    },
  };
  </script>
  
  <style scoped>
  .pricing-card {
    padding: 20px;
    background-color: #f3f4f6;
    color: #333;
    text-align: center;
  }
  
  .highlight-card {
    background-color: #6a0dad;
    color: #fff;
  }
  
  .title {
    font-weight: bold;
    font-size: 1.2em;
    margin-bottom: 10px;
  }
  
  .price {
    font-size: 2em;
    font-weight: bold;
    margin-bottom: 10px;
  }
  
  .features {
    list-style: none;
    padding: 0;
    margin: 0;
  }
  
  .features li {
    margin-bottom: 8px;
  }
  
  .start-btn {
    margin-top: 20px;
  }
  </style>
  