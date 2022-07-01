<template>
  <IndexCard
    title="Un poco de mi"
    image="https://cdn.pixabay.com/photo/2015/12/04/14/05/code-1076536_960_720.jpg"
    :paragraphs="indexText"
  />
</template>

<script setup lang="ts">
const indexText = ref([
  "En esta sección se encuentran algunos ejemplos de proyectos que he realizado.",
  "Algunos de ellos",
]);
</script>

<style scoped></style>
