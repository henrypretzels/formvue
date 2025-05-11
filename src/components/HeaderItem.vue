<template>
  <header>
    <nav>
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/about">About</RouterLink>
      <RouterLink to="/test">Teste</RouterLink>
    </nav>
  </header>
</template>

<script setup lang="ts">
// You can import any necessary components or libraries here
</script>

<style scoped>
/* Add any styles specific to this component here */
nav {
  /* Example styles */
  display: flex;
  gap: 1rem;
}
</style>
