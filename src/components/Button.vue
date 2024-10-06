<script setup>
import { defineProps } from 'vue';

const props = defineProps({
  label: {
    type: String,
    required: true,
  },
  iconURL: {
    type: String,
    default: null,
  },
  backgroundColor: {
    type: String,
    default: '',
  },
  textColor: {
    type: String,
    default: '',
  },
  borderColor: {
    type: String,
    default: '',
  },
  fullWidth: {
    type: Boolean,
    default: false,
  },
});
</script>

<template>
    <button
      :class="[
        'flex justify-center items-center gap-2 px-7 py-4 border font-montserrat text-lg leading-none rounded-full',
        backgroundColor ? [backgroundColor, textColor, borderColor] : 'bg-coral-red text-white border-coral-red',
        fullWidth ? 'w-full' : ''
      ]"
    >
      {{ label }}
      <img
        v-if="iconURL"
        :src="iconURL"
        alt="arrow right icon"
        class="ml-2 rounded-full bg-white w-5 h-5"
      />
    </button>
  </template>
  

  
  <style scoped>
  /* Add custom styles if necessary */
  </style>
  