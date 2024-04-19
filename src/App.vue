<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header class="header navbar navbar-expand-lg bg-light shadow-sm fixed-top">
    <div class="container px-3">
      <a href="#" class="navbar-brand pe-3">
        <img src="@/assets/logo.svg"  width="47" alt="Silicon">
        Women Techmakers Maputo
      </a>
    </div>
  </header>

  <RouterView />
</template>

<style scoped>

</style>
