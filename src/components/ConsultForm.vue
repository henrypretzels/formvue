<template>
  <form @submit.prevent="handleSubmit" class="consult-form">
    <h2>Faça uma requisição</h2>
    <div>
      <label for="name">Nome:</label>
      <input type="text" id="name" v-model="formData.name" required />
    </div>
    <div>
      <label for="email">Email:</label>
      <input type="email" id="email" v-model="formData.email" required />
    </div>
    <div>
      <label for="message">Mensagem:</label>
      <textarea id="message" v-model="formData.message" required></textarea>
    </div>
    <button type="submit">Enviar</button>
  </form>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const formData = ref({
  name: '',
  email: '',
  message: '',
})

const handleSubmit = () => {
  console.log('Form submitted:', formData.value)
  formData.value = { name: '', email: '', message: '' }
}
</script>
