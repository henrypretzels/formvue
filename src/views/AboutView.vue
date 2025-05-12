
<template>
  <div class="about-container">
    <div class="content">
      <h1>Sobre a Empresa</h1>
      <p>
        Fundada em Janeiro de 2025, a <strong>GHJ Automação</strong> é uma empresa inovadora focada em soluções web.
        Nosso objetivo é simplificar o desenvolvimento de interfaces ricas e dinâmicas
        usando tecnologias como Vue.js e Vite.
      </p>
      <p>
        Fundada por entusiastas da programação, acreditamos que a web deve ser
        acessível, rápida e elegante. Desenvolvemos ferramentas, bibliotecas e
        tutoriais que ajudam grandes corporações a otimizar seus processos.
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'About'
}
</script>

<style scoped>
.about-container {
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #f4f4f4;
}

.content {
  max-width: 600px;
  padding: 20px;
  background-color: white;
  border-radius: 8px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
}

.content h1 {
  margin-bottom: 16px;
  color: #42b983;
}

.content p {
  margin-bottom: 12px;
  line-height: 1.6;
  color: #333;
}
</style>
