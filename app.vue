<template>
  <div data-theme="forest">
    <Layout :title="title">
      <NuxtPage />
      <Footer />
    </Layout>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";

useHead({
  titleTemplate: (title) => `${title} - JigoDev `,
});
const title = ref("Octavio Jiménez - Full Stack Developer");
</script>
