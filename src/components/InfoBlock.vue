<template>
  <div class="info-block">
    <h2>{{ title }}</h2>
    <p>{{ content }}</p>
    <ul>
      <li v-for="(item, index) in items" :key="index">{{ item }}</li>
    </ul>
  </div>
</template>

<script setup lang="ts">
defineProps<{
  title: string
  items: string[]
  content: string
}>()
</script>

<style scoped>
.info-block {
  border: 1px solid #ccc;
  padding: 1rem;
  margin: 1rem 0;
  border-radius: 5px;
  display: block;
  align-items: auto;
}
h2 {
  margin-bottom: 0.5rem;
}
ul {
  list-style-type: disc;
  padding-left: 1.5rem;
}
</style>
