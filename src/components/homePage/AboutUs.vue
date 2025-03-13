<script setup>
import ButtonComponent from '@/components/composables/ButtonComponent.vue';
</script>

<template>
  <div class="relative w-full md:h-screen">
    <div class="sm:absolute bg-[#10b981] w-full sm:w-2/3 md:h-[92%] top-0 right-0 pb-10">
      <div class="w-full sm:absolute -inset-x-1/3 inset-y-20 mb-4 md:mb-0">
        <img
          src="../../assets/images/about.jpg"
          alt="about us"
          class="md:max-w-[32rem] h-auto object-cover"
        />
      </div>
      <div
        class="text-white px-4 sm:absolute right-1/4 sm:w-2/4 sm:transform sm:top-2/4 sm:-translate-y-2/4"
      >
        <h2 class="text-sm font-semibold mb-4 uppercase tracking-wide">About Us</h2>
        <h1 class="text-2xl md:text-4xl font-semibold mb-4">Welcome to Carbook</h1>
        <p class="text-base mb-6">
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Culpa expedita laborum enim
          molestias perferendis velit minus hic reprehenderit? Error, quasi? Ipsum, hic eum.
          Accusamus, dolor placeat quod aliquam perferendis optio.
        </p>
        <p class="text-base">
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Culpa expedita laborum enim
          molestias perferendis velit minus hic reprehenderit? Error, quasi? Ipsum, hic eum.
          Accusamus, dolor placeat quod aliquam perferendis optio.
        </p>
        <ButtonComponent text="Search Vechicle" />
      </div>
    </div>
  </div>
</template>
