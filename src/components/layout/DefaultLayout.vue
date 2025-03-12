<script setup>
import PageHeader from '@/components/layout/PageHeader.vue';
import PageFooter from '@/components/layout/PageFooter.vue';
</script>

<template>
  <div class="min-h-screen flex flex-col relative">
    <PageHeader />
    <main class="flex-grow">
      <router-view />
    </main>
    <PageFooter />
  </div>
</template>
