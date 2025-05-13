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
