<script setup>
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/swiper-bundle.css';
import { Autoplay } from 'swiper/modules';
import 'swiper/css/autoplay';
import SectionHeading from '@/components/composables/SectionHeading.vue';
import { testimony } from '@/data/testimonyData';
</script>

<template>
  <div class="bg-gray-100/90">
    <SectionHeading title="Happy Clients" description="Testimonial" />
    <section>
      <swiper
        :modules="[Autoplay]"
        :space-between="30"
        navigation
        loop
        :autoplay="{ delay: 3000, disableOnInteraction: false }"
        :breakpoints="{
          640: { slidesPerView: 2 },
          1024: { slidesPerView: 3 },
        }"
        class="w-full max-w-5xl"
      >
        <swiiper-slide>
            <TestimonyCard />
        </swiiper-slide>    
    </swiper>
    </section>
  </div>
</template>
