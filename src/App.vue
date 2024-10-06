<script setup>

 import Nav from '@/components/Nav.vue';
import Hero from '@/components//Hero.vue';
import PopularProducts from '/sections/PopularProducts.vue';
import SuperQuality from '../sections/SuperQuality.vue';
import Services from '../sections/Services.vue';
import SpecialOffer from '../sections/SpecialOffer.vue';
import CustomerReviews from '../sections/CustomerReviews.vue';
import Subscribe from './components/Subscribe.vue';
import Footer from '/sections/Footer.vue';
</script>

<template>
  <main class="relative">
  <Nav></Nav> 
    <section class="xl:padding-l wide:padding-r padding-b">
      <Hero></Hero> 
    </section>
    <section class="padding">
      <PopularProducts/>
    </section>
    <section class="padding">
      <SuperQuality/> 
    </section>
    <section class="padding-x py-10">
      <Services/> 
    </section>
    <section class="padding">
      <SpecialOffer/>
    </section>
    <section class="bg-pale-blue padding">
<CustomerReviews/>
    </section>
    <section class="padding-x sm:py-32 py-16 w-full">
      <Subscribe/>
    </section>
    <section class="bg-black padding-x padding-t pb-8">
   <Footer></Footer>
    </section>
  </main>
</template>

