<template>
  <div>
    <Layout :title="title">
      <NuxtPage />
    </Layout>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";

const title = ref("Octavio Jiménez - Full Stack Developer");
</script>
