<script setup>
import BgContainer from '@/components/composables/BgContainer.vue';
import AboutUs from '@/components/homePage/AboutUs.vue';
import CallToAction from '@/components/homePage/CallToAction.vue';
import TestimonySection from '@/components/homePage/TestimonySection.vue';
import StatisticsSection from '@/components/homePage/StatisticsSection.vue';
</script>

<template>
  <BgContainer
    title="About"
    bgImage="bg_3.jpg"
    :links="[
      { text: 'Home', to: '/' },
      { text: 'About Us', to: '/about' },
    ]"
  />
  <AboutUs />
  <CallToAction />
  <TestimonySection />
  <StatisticsSection />
</template>
