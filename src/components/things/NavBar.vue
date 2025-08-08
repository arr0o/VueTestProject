<template>
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

<style scoped>
</style>
