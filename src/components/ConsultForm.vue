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

<style scoped>
.consult-form {
  border: 1px solid #ccc;
  margin: auto;
}

h2 {
  margin-bottom: 1rem;
}

div {
  margin-bottom: 1rem;
}

label {
  display: float;
  margin-bottom: 0.5rem;
}

input,
textarea {
  width: 100%;
  padding: 0.5rem;
  border: 1px solid #ccc;
  border-radius: 4px;
}

button {
  padding: 0.5rem 1rem;
  background-color: #007bff;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

button:hover {
  background-color: #0056b3;
}
</style>
