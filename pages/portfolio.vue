<template>
  <div>
    <Tabs :links="links" />
    <NuxtPage />
  </div>
</template>

<script setup lang="ts">
import { Ref } from "vue";
import { LinkListItem } from "models";

useHead({
  title: "Portafolio",
});

const links: Ref<LinkListItem[]> = ref([
  {
    text: "Inicio",
    link: "/portfolio",
  },
  {
    text: "Full-Stack",
    link: "/portfolio/full_stack",
  },
  {
    text: "Backend",
    link: "/portfolio/backend",
  },
  {
    text: "Frontend",
    link: "/portfolio/frontend",
  },
]);
</script>

<style scoped></style>
