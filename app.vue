<template>
  <div>
    <Layout :title="title">
      <NuxtPage />
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
