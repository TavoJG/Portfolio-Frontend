<template>
  <div class="container mx-auto">
    <IndexCard
      title="Un poco de mi"
      image="https://cdn.pixabay.com/photo/2015/12/04/14/05/code-1076536_960_720.jpg"
      :paragraphs="cardText"
    />
    <div class="divider"></div>
    <AboutMeSkillsCard />
  </div>
</template>

<script setup lang="ts">
import { ref, Ref } from "vue";

useHead({
  title: "Acerca de mi",
});

const cardText = ref([
  ` Actualmente trabajo como desarrollador web Full-Stack, y cuento con más
        de cuatro años de experiencia. Me considero un apasionado de la ciencia
        y tecnología. Soy una persona que ama su trabajo, y siempre esta
        dispuesta a ayudar.`,
]);
</script>

<style scoped></style>
