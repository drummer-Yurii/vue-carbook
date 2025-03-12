<script setup>
import { computed, onBeforeUnmount, onMounted, ref } from 'vue';

const isScrolled = ref(false);
const isMobile = ref(window.innerWidth < 760);

const carClass = computed(() => {
  if (isMobile.value) return 'text-black';
  return isScrolled.value ? 'text-black' : 'text-white';
});

const handleScroll = () => {
  isScrolled.value = window.scrollY > 50;
};

onMounted(() => {
  window.addEventListener('scroll', handleScroll);
});
onBeforeUnmount(() => {
  window.removeEventListener('scroll', handleScroll);
});
</script>

<template>
  <router-link to="/">
    <h1 class="uppercase text-xl font-bold cursor-pointer">
      <span :class="carClass">Car</span>
      <span class="text-green-500">Book</span>
    </h1>
  </router-link>
</template>
