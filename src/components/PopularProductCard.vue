<script>
  import { star } from "../assets/icons";
  
  export default {
    name: "PopularProductCard",
    props: {
      imgURL: {
        type: String,
        required: true,
      },
      name: {
        type: String,
        required: true,
      },
      price: {
        type: String,
        required: true,
      },
    },
    data() {
      return {
        star,
      };
    },
  };
  </script>
<template>
    <div class="flex flex-1 flex-col w-full max-sm:w-full">
      <img :src="imgURL" :alt="name" class="w-[282px] h-[282px]" />
      <div class="mt-8 flex justify-start gap-2.5">
        <img :src="star" alt="rating icon" width="24" height="24" />
        <p class="font-montserrat text-xl leading-normal text-slate-gray">
          (4.0)
        </p>
      </div>
      <h3 class="mt-2 text-2xl leading-normal font-semibold font-palanquin">
        {{ name }}
      </h3>
      <p class="mt-2 font-semibold font-montserrat text-coral-red text-2xl leading-normal">
        {{ price }}
      </p>
    </div>
  </template>
  
  
  
  <style scoped>
  /* Add your styles here if needed */
  </style>
  