<script setup>
import SectionHeading from '@/components/composables/SectionHeading.vue';
import CarCards from '@/components/cards/CarCards.vue';
import { cars } from '@/data/carsData';
</script>

<template>
    <SectionHeading description="What we offer" title="Featured Vechicles" />
    <div v-for="(car, index) in cars" :key="index">
        <CarCards :id="car.id" :name="car.name" :brand="car.brand" :price="car.price" :image="car.image" />
    </div>
</template>