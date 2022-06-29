<template>
  <div class="card lg:card-side bg-base-100 shadow-xl">
    <div class="card-body">
      <h2 class="card-title">Habilidades de desarrollo</h2>
      <div class="columns-1 sm:columns-2 md:columns-3">
        <AboutMeSkillCard
          v-for="(skill, i) in skillList"
          :key="i"
          :title="skill.title"
          :content="skill.items"
        />
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref, Ref } from "vue";
import { SkillsItem } from "@/models";

const skillList: Ref<SkillsItem[]> = ref([
  {
    title: "Python",
    items: ["Django", "Django Rest Framework", "Flask", "FastAPI"],
  },
  {
    title: "JavaScript",
    items: ["NodeJS", "Typescript", "ExpressJS", "VueJS", "NuxtJS"],
  },
  { title: "APIs", items: ["REST", "GraphQL"] },
  {
    title: "Bases de datos",
    items: ["PostgreSQL", "PostGIS", "MySQL", "MongoDB", "Redis"],
  },
  {
    title: "Cloud",
    items: ["Google Cloud Platform", "Amazon Web Services"],
  },
  {
    title: "Infraestructura",
    items: ["Docker", "Docker Compose", "Terraform"],
  },
  {
    title: "CI/CD",
    items: ["GitHub Actions", "Jenkins", "GCP Cloud Build", "AWS Codebuild"],
  },
  {
    title: "Others",
    items: ["Gitflow", "AGILE", "GIS", "Análisis de datos"],
  },
]);
</script>

<style scoped></style>
