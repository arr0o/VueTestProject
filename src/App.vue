<script setup lang="ts">
import { RouterView } from 'vue-router'
import NavBar from './components/NavBar.vue';
</script>

<template>
  <header>
    <NavBar />
  </header>
  <h1>VueTestProject</h1>
  <RouterView />
</template>

<style scoped>
</style>
