<script setup>
import { onMounted, ref } from 'vue';
import bgImage from '../../assets/images/bg_1.jpg';

const isVisible = ref(false);

onMounted(() => { 
  setTimeout(() => { 
    isVisible.value = true;
  }, 100);
});
</script>

<template>
  <section class="bg-cover relative h-screen" :style="{ backgroundImage: `url(${bgImage})` }">
    <div class="absolute inset-0 bg-black opacity-25"></div>
    <div class="relative flex items-center justify-center h-full text-center text-white px-4">
      <div class="w-full md:w-3/5 content-wrapper" :class="{ 'animate-in': isVisible }">
        <h1 class="text-4xl md:text-5xl font-bold mb-4">Fast & Ease Way To Rent A Car</h1>
        <p class="text-md md:text-xl mb-6">
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ut quisquam doloremque sequi
          dolorum voluptatum saepe.
        </p>
        <h2 class="text-2xl font-semibold">Ease steps for renting a car</h2>
      </div>
    </div>
  </section>
</template>

<style>
.content-wrapper {
  transform: translateY(80px);
  opacity: 0;
  transition: all 1s ease-out;
}
.content-wrapper.animate-in {
  transform: translateY(0);
  opacity: 1;
}
</style>