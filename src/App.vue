<script setup lang="ts">
import { RouterView } from 'vue-router'
import Button from 'primevue/button';

const toggleDarkMode = () => {
  console.log("toggleDarkMode: ", document.documentElement.classList.toggle('app-dark'));
  document.documentElement.classList.toggle('app-dark');
}
</script>

<template>
  <header>
    <h1>VueTestProject</h1>
  </header>
  <div class="button-div justify-center">
    <Button label="Toggle Dark Mode" @click="toggleDarkMode" />
  </div>
  <RouterView />
</template>

<style scoped>
/* @tailwind base;
@tailwind components;
@tailwind utilities; */
header {
  margin-bottom: 100px;
}

.button-div {
  display: flex;
  background-color: var(--p-surface-100);
}
</style>
