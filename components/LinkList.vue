<template>
  <li v-for="(link, i) in linkList" :key="i">
    <NuxtLink :to="link.link">{{ link.text }}</NuxtLink>
  </li>
</template>

<script setup lang="ts">
import { ref, Ref } from "vue";
import { LinkListItem } from "models";

const linkList: Ref<LinkListItem[]> = ref([
  {
    text: "Inicio",
    link: "/",
  },
  {
    text: "Acerca de nosotros",
    link: "/about_us",
  },
  {
    text: "Portafolio",
    link: "/portfolio",
  },
]);
</script>

<style scoped></style>
