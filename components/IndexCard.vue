<template>
  <div class="card lg:card-side bg-base-100 shadow-xl">
    <figure>
      <img :src="image" alt="Album" />
    </figure>
    <div class="card-body">
      <h2 class="card-title">{{ title }}</h2>
      <p v-for="(text, i) in paragraphs" :key="i">
        {{ text }}
      </p>
    </div>
  </div>
</template>

<script setup lang="ts">
defineProps<{
  image: string;
  title: string;
  paragraphs: string[];
}>();
</script>

<style scoped></style>
