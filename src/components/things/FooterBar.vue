<template>
    <footer class="text-gray-400 bg-green-100 footer">
        <p class="footer_copy-right">&copy; 2023 VueTestProject. All rights reserved.</p>
        <nav class="footer_main-nav">
            <ul class="footer_main-nav_items">
                <li class="footer_main-nav_item"><router-link to="/">Home</router-link></li>
                <li class="footer_main-nav_item"><router-link to="/about">About</router-link></li>
            </ul>
        </nav>
    </footer>
</template>

<script setup lang="ts">
</script>

<style scoped>
    .footer {
        position: fixed;
        bottom: 0px;
        width: 100%;
    }

    .footer > * {
        display: inline-block;
        vertical-align: middle;
    }

    .footer_main-nav {
        display: inline-block;
        text-align: center;
        width: calc(100% - 285px);
        vertical-align: middle;
    }

    .footer_main-nav_items {
        margin: 0;
        padding: 0;
        list-style: none;
    }

    .footer_main-nav_item {
        display: inline-block;
        margin: 0px 8px;
    }

    .footer_main-nav_item a {
        text-decoration: none;
        color: #0e4f1f;
        font-weight: bold;
        padding: 3px 0px;
    }

    .footer_main-nav_item a:hover,
    .footer_main-nav_item a:active {
        color: white;
        border-bottom: 5px solid white;
    }
</style>