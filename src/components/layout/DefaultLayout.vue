<script setup>
import PageHeader from '@/components/layout/PageHeader.vue';
import PageFooter from '@/components/layout/PageFooter.vue';
</script>

<template>
  <PageHeader />
  <main>
    <router-view />
  </main>
  <PageFooter />
</template>
