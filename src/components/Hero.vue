<script setup>
import { ref } from "vue";
import { shoes, statistics } from "@/constants"; // Import constants
import { bigShoe1 } from "@/assets/images"; // Import image
import { arrowRight } from "@/assets/icons"; // Import icon
import Button from "@/components/Button.vue"; // Import Button component
import ShoeCard from "@/components/ShoeCard.vue"; // Import ShoeCard component

// State
const bigShoeImg = ref(bigShoe1);

// Function to change big shoe image
const changeBigShoeImage = (shoe) => {
  bigShoeImg.value = shoe;
};
</script>

<template>
  <section id="home" class="w-full flex xl:flex-row flex-col justify-center min-h-screen gap-10 max-container">
    <!-- Left section: Text content -->
    <div class="relative xl:w-2/5 flex flex-col justify-center items-start w-full max-xl:padding-x pt-28">
      <p class="text-xl font-montserrat text-coral-red">
        Our Summer collections
      </p>
      <h1 class="mt-10 font-palanquin text-8xl max-sm:text-[72px] max-sm:leading-[82px] font-bold">
        <span class="xl:bg-white xl:whitespace-nowrap relative z-10 pr-10">
          The New Arrival
        </span>
        <br />
        <span class="text-coral-red inline-block mt-3">Nike</span> Shoes
      </h1>
      <p class="font-montserrat text-slate-gray text-lg leading-8 mt-6 mb-14 sm:max-w-sm">
        Discover stylish Nike arrivals, quality comfort, and innovation for
        your active life.
      </p>
      <Button label="Shop now" :iconURL="arrowRight" />
      <div class="flex justify-start items-start flex-wrap w-full mt-20 gap-16">
        <div v-for="(stat, index) in statistics" :key="index">
          <p class="text-4xl font-palanquin font-bold">{{ stat.value }}</p>
          <p class="leading-7 font-montserrat text-slate-gray">{{ stat.label }}</p>
        </div>
      </div>
    </div>

    <!-- Right section: Shoe images -->
    <div class="relative flex-1 flex justify-center items-center xl:min-h-screen max-xl:py-40 bg-primary bg-hero bg-cover bg-center">
      <img
        :src="bigShoeImg"
        alt="shoe collection"
        width="610"
        height="502"
        class="object-contain relative z-10"
      />
      <div class="flex sm:gap-6 gap-4 absolute -bottom-[5%] sm:left-[10%] max-sm:px-6">
        <div v-for="(image, index) in shoes" :key="index">
          <ShoeCard
            :index="index"
            :imgURL="image"
            @changeBigShoeImage="changeBigShoeImage"
            :bigShoeImg="bigShoeImg"
          />
        </div>
      </div>
    </div>
  </section>
</template>


<style scoped>
/* Add any component-specific styling here */
</style>