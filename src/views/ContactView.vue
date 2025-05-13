<template>
  <div class="contact-page">
    <h1>Fale Conosco</h1>
    <p>
      Entre em contato conosco para solicitar uma consultoria ou tirar dúvidas sobre nossos
      serviços.
    </p>

    <ConsultForm />
    <p>Ou envie um e-mail diretamente, em caso de dúvidas mais específicas:</p>
    <a href="mailto:contato@ghjautomacao.com" class="contact-email">contato@ghjautomacao.com</a>
  </div>
</template>

<script setup lang="ts">
import ConsultForm from '../components/ConsultForm.vue'
</script>

<style scoped>
.contact-page {
  max-width: 700px;
  margin: auto;
  padding: 2rem 1rem;
}
</style>
