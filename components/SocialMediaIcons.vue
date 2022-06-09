<template>
  <div>
    <button
      v-for="(button, i) in buttonList"
      :key="i"
      class="btn btn-square btn-ghost"
      @click="goTo(button.link)"
    >
      <i class="mdi" :class="button.icon" aria-hidden="true"></i>
    </button>
  </div>
</template>

<script setup lang="ts">
import { ref } from "vue";

const buttonList = ref([
  {
    link: "http://www.google.com",
    icon: "mdi-facebook",
  },
  {
    link: "http://www.google.com",
    icon: "mdi-instagram",
  },
  {
    link: "http://www.google.com",
    icon: "mdi-github",
  },
]);

const goTo = (link: string) => {
  window.open(link);
};
</script>

<style lang="scss" scoped></style>
