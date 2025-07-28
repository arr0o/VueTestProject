<script setup lang="ts">
import Menubar from 'primevue/menubar';
import { ref } from "vue";

const menuItems = ref([
    {
        label: 'Home',
        icon: 'pi pi-home',
        route: '/'
    },
    {
        label: 'About',
        icon: 'pi pi-headphones',
        route: '/about'
    }
]);
</script>

<template>
  <!-- <header class="main-header">
      <div>
          <li class="main-nav_item"><router-link :to="{name: 'Home'}">Home</router-link></li>
      </div>
      <nav class="main-nav">
          <ul class="main-nav_items">
            <li class="main-nav_item"><router-link :to="{name: 'About'}">About</router-link></li>
          </ul>
      </nav>
  </header> -->
  <Menubar :model="menuItems">
    <template #item="{ item, props }">
                <router-link v-if="item.route" v-slot="{ href, navigate }" :to="item.route" custom>
                    <a v-ripple :href="href" v-bind="props.action" @click="navigate">
                        <span :class="item.icon" />
                        <span>{{ item.label }}</span>
                    </a>
                </router-link>
                <a v-else v-ripple :href="item.url" :target="item.target" v-bind="props.action">
                    <span :class="item.icon" />
                    <span>{{ item.label }}</span>
                </a>
            </template>
  </Menubar>
</template>

<style scoped>
  .main-header {
      background-color: #2ddf5c;
      width: 100%;
      padding: 10px 16px;
      position: fixed;
      top: 0;
      z-index: 100;
  }

  .main-header > div {
      display: inline-block;
      vertical-align: middle;
  }

  .main-nav {
      display: inline-block;
      text-align: right;
      width: calc(100% - 74px);
      vertical-align: middle;
  }

  .main-nav_items {
      margin: 0;
      padding: 0;
      list-style: none;
  }

  .main-nav_item {
      display: inline-block;
      margin: 0px 8px;
  }

  .main-nav_item a {
      text-decoration: none;
      color: #0e4f1f;
      font-weight: bold;
      padding: 3px 0px;
  }

  .main-nav_item a:hover,
  .main-nav_item a:active {
      color: white;
      border-bottom: 5px solid white;
  }

  .main-nav_item--cta a {
      color: white;
      background: #ff1b68;
      padding: 8px 16px;
      border-radius: 8px;
  }

  .main-nav_item--cta a:hover,
  .main-nav_item--cta a:active {
      color: #ff1b68;
      background: white;
      border: none;
  }
</style>
