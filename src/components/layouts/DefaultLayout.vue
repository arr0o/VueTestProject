<template>
    <div>
        <NavBar />
        <router-view />
        <FooterBar />
    </div>
</template>

<script setup lang="ts">
    import NavBar from '@/components/things/NavBar.vue';
    import FooterBar from '@/components/things/FooterBar.vue';
</script>

<style scoped>

</style>