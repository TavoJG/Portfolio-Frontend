<template>
  <div>
    <li v-for="(link, i) in linkList" :key="i">
      <NuxtLink :to="link.link">{{ link.text }}</NuxtLink>
    </li>
  </div>
</template>

<script setup lang="ts">
import { ref, Ref } from "vue";
import { LinkListItem } from "models";

const linkList: Ref<LinkListItem[]> = ref([
  {
    text: "Inicio",
    link: "/",
  },
]);
</script>

<style scoped></style>
