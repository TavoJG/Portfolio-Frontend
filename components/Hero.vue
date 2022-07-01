<template>
  <div
    class="hero min-h-screen"
    style="
      background-image: url(https://cdn.pixabay.com/photo/2016/11/30/20/58/programming-1873854_960_720.png);
    "
  >
    <div class="hero-overlay bg-opacity-60"></div>
    <div class="hero-content text-center text-neutral-content">
      <div class="max-w-md">
        <h1 class="mb-5 text-5xl font-bold">Fabricamos tus ideas</h1>
        <p class="mb-5">
          Provident cupiditate voluptatem et in. Quaerat fugiat ut assumenda
          excepturi exercitationem quasi. In deleniti eaque aut repudiandae et a
          id nisi.
        </p>
        <button class="btn btn-primary" @click="buttonClick">Conoce más</button>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
const buttonClick = () => {
  navigateTo("/about_me");
};
</script>

<style scoped></style>
