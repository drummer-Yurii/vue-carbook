<script setup>
import { onMounted, ref } from 'vue';
import { useRoute } from 'vue-router';
import BgContainer from '@/components/composables/BgContainer.vue';
import BlogComments from '@/components/composables/BlogComments.vue';
import { blogs } from '@/data/blogData';

const route = useRoute();
const blog = ref(null);

const getImage = (imageName) => {
  return new URL(`/src/assets/images/${imageName}`, import.meta.url).href;
};

onMounted(() => {
  const blogId = Number(route.params.id);
  blog.value = blogs.find((b) => b.id === blogId) || {};
});
</script>

<template>
  <BgContainer
    title="Blog Details"
    bgImage="bg_3.jpg"
    :links="[
      { text: 'Home', to: '/' },
      { text: 'Blogs', to: '/blogs' },
    ]"
  />
  <div v-if="blog" class="flex justify-center p-4 py-10 md:py-20">
    <div class="md:w-4/5">
      <h1 class="text-2xl md:text-4xl font-medium text-gray-800 mb-2">{{ blog.title }}</h1>
      <p class="text-sm text-blue-500 mb-6">
        {{ blog.date }}
        {{ blog.author }}
        {{ blog.comment?.length }} Comments
      </p>
      <img :src="getImage(blog.image)" alt="blog-image" class="w-full md:h-[600px]" />
      <p class="text-gray-400 my-6">{{ blog.description }}</p>
      <div v-if="blog.comments?.length">
        <BlogComments v-for="(comment, index) in blog.comments" :key="index" :comment="comment" />
      </div>
      <p class="text-gray-400 my-6" v-else>No comments yet. Be the first to leave a comment!</p>
    </div>
  </div>
</template>
