<template>
  <div class="card shadow-xl">
    <div class="card-body">
      <h2 class="card-title">{{ title }}</h2>
      <ul class="list-disc">
        <li v-for="(item, i) in content" :key="i">
          {{ item }}
        </li>
      </ul>
    </div>
  </div>
</template>

<script setup lang="ts">
defineProps<{
  title: string;
  content: string[];
}>();
</script>

<style scoped></style>
