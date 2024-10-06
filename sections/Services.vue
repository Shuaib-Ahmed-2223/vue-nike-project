<script setup>
// Import the constants and components
import { services } from '@/constants';
import ServiceCard from '@/components/ServiceCard.vue';
</script>

<template>
<section class="max-container flex justify-center flex-wrap gap-8">
  <div v-for="service in services" :key="service.label">
    <ServiceCard v-bind="service" />
  </div>
</section>
  </template>
  
 
  
  <style scoped>
  /* Add any necessary scoped styles */
  </style>
  