<template>
  <div id="app">
    <header class="fixed top-0 left-0 w-full bg-white dark:bg-gray-800 shadow-md z-50">
      <nav class="p-4 flex gap-4">
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">Sobre</RouterLink>
        <RouterLink to="/login">Login</RouterLink>
      </nav>
      <button @click="darkMode = !darkMode">
        {{ darkMode ? 'Modo Claro' : 'Modo Escuro' }}
      </button>
    </header>

    <main class="pt-20 px-4" style="max-width: 1000px; margin: auto">
      <RouterView />
    </main>
  </div>
</template>

<script setup lang="ts">
import { ref, watch } from 'vue'

const darkMode = ref(false)

watch(darkMode, (value) => {
  document.body.classList.toggle('dark', value)
})
</script>

<style scoped>
nav a {
  text-decoration: none;
  color: inherit;
}

nav a:hover {
  text-decoration: underline;
}
</style>
