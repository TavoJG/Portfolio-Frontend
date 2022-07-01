<template>
  <div>
    <a
      v-for="(button, i) in buttonList"
      :key="i"
      class="btn btn-square btn-ghost mdi"
      :class="button.icon"
      aria-hidden="true"
      @click="goTo(button.link)"
    >
    </a>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";

const buttonList = ref([
  {
    link: "https://www.facebook.com/jigodevs",
    icon: "mdi-facebook",
  },
  {
    link: "http://www.google.com",
    icon: "mdi-instagram",
  },
  {
    link: "https://github.com/TavoJG/Portfolio-Frontend",
    icon: "mdi-github",
  },
]);

const goTo = (link: string) => {
  window.open(link);
};
</script>

<style lang="scss" scoped></style>
