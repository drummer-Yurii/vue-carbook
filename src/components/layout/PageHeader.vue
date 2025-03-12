<script setup>
import { useRoute } from 'vue-router';
import PageLogo from '@/components/composables/PageLogo.vue';

const route = useRoute();

const links = [
  { name: 'Home', path: '/' },
  { name: 'About', path: '/about' },
  { name: 'Services', path: '/services' },
  { name: 'Pricing', path: '/pricing' },
  { name: 'Cars', path: '/cars' },
  { name: 'Blog', path: '/blog' },
  { name: 'Contact', path: '/contact' },
];
</script>

<template>
  <header class="flex justify-center px-6 p-2">
    <div class="flex justify-between items-center w-full md:w-5/6 md:relative z-50">
      <PageLogo />
      <nav class="space-x-6">
        <router-link
          v-for="link in links"
          :key="link.path"
          :to="link.path"
          :class="{ 'active-link': route.path === link.path }"
        >
          {{ link.name }}
        </router-link>
      </nav>
    </div>
  </header>
</template>
