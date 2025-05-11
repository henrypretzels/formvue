<script setup lang="ts">
import InfoBlock from '../components/InfoBlock.vue'
import ConsultForm from '../components/ConsultForm.vue'

const infoBlockItems = [
  'Integração de CLPs e sensores',
  'Sistemas supervisórios SCADA',
  'Internet das Coisas (IoT) para aplicações residenciais e industriais',
  'Manutenção preditiva com IA',
  'Suporte e assistência técnica',
]

const infoBlockContent = `Na GHJ Automação, unimos eficiência e inovação para transformar processos industriais ou facilitar a sua rotina com soluções inteligentes. Nossa equipe é especializada em identificar oportunidades de melhoria, propor tecnologias adequadas e acompanhar a implantação de cada projeto do início ao fim. Conheça algumas das áreas em que podemos atuar, e caso esteja interessado, solicite uma consultoria gratuíta nos campos abaixo.:`
</script>

<template>
  <div class="container">
    <InfoBlock
      :title="'Soluções em Automação'"
      :items="infoBlockItems"
      :content="infoBlockContent"
    />
    <ConsultForm />
  </div>
</template>

<style scoped>
.container {
  padding: 1rem;
  max-width: 800px;
  margin: auto;
}
/* Include any other CSS adaptations here */
</style>
