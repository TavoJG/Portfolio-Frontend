<template>
  <div class="tabs">
    <NuxtLink
      v-for="(link, i) in links"
      :key="i"
      class="tab tab-bordered"
      :class="{ 'tab-active': isActiveRoute(link.link) }"
      :to="link.link"
      >{{ link.text }}</NuxtLink
    >
  </div>
</template>

<script setup lang="ts">
import { LinkListItem } from "models";

defineProps<{
  links: LinkListItem[];
}>();

const isActiveRoute = (link: string): boolean => useRoute().path == link;
</script>

<style lang="scss" scoped></style>
