<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <header class="header navbar navbar-expand-lg bg-light shadow-sm fixed-top">
    <div class="container px-3">
      <a href="#" class="navbar-brand pe-3">
        <img src="@/assets/logo.svg"  width="47" alt="Silicon">
        Silicon
      </a>
    </div>
  </header>

  <RouterView />
</template>

<style scoped>

</style>
