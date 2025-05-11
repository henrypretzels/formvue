<script setup lang="ts">
import { RouterLink } from 'vue-router'
</script>

<template>
  <h1>Hello</h1>
  <div></div>
  <nav>
    <RouterLink to="/">Home</RouterLink>
    <RouterLink to="/about">About</RouterLink>
    <RouterLink to="/login">Login</RouterLink>
  </nav>

  <RouterView />
</template>
