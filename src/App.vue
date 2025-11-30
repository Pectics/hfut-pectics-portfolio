<template>
  <div class="app-shell">
    <Navbar />
    <main class="page-container">
      <RouterView />
    </main>
    <FooterBar />
  </div>
</template>

<script setup>
import { RouterView } from 'vue-router'
import Navbar from './components/Navbar.vue'
import FooterBar from './components/Footer.vue'
</script>
