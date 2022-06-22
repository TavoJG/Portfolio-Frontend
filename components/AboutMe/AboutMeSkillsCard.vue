<template>
  <div class="card lg:card-side bg-base-100 shadow-xl">
    <div class="card-body">
      <h2 class="card-title">Habilidades de desarrollo</h2>
      <ul class="list-disc">
        <li v-for="(item, i) in skillList" :key="i">
          <span class="font-bold">{{ item.title }}</span>
          <ul class="list-disc">
            <li v-for="(skill, j) in item.items" :key="j">
              {{ skill }}
            </li>
          </ul>
        </li>
      </ul>
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

<style scoped>
ul > li {
  margin-left: 15px;
}
</style>
