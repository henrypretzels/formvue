<script setup lang="ts">
import InfoBlock from '../components/InfoBlock.vue'
import { ref, onMounted } from 'vue'

const testimonials = ref([])

onMounted(async () => {
  const res = await fetch('http://localhost:3000/testimonials')
  testimonials.value = await res.json()
})

const infoBlockItems = [
  'Integração de CLPs e sensores',
  'Sistemas supervisórios SCADA',
  'Internet das Coisas (IoT) para aplicações residenciais e industriais',
  'Manutenção preditiva com IA',
  'Suporte e assistência técnica',
]

const infoBlockContent = `Na GHJ Automação, unimos eficiência e inovação para transformar processos industriais ou facilitar a sua rotina com soluções inteligentes. Nossa equipe é especializada em identificar oportunidades de melhoria, propor tecnologias adequadas e acompanhar a implantação de cada projeto do início ao fim. Conheça algumas das áreas em que podemos atuar, e caso esteja interessado, solicite uma consultoria gratuita nos campos abaixo:`

// const testimonials = [
//   { name: 'João S.', content: 'Profissionais incríveis e suporte impecável. Recomendo muito!' },
//   { name: 'Empresa XYZ', content: 'Reduzimos 40% dos custos com as soluções da GHJ.' },
//   { name: 'Maria A.', content: 'Me ajudaram a automatizar minha linha de produção com IoT!' },
// ]

const benefits = [
  'Atendimento personalizado',
  'Equipe multidisciplinar',
  'Uso de tecnologias emergentes',
  'Agilidade na entrega de projetos',
  'Consultoria gratuita inicial',
]
</script>

<template>
  <div class="container">
    <InfoBlock
      :title="'Soluções em Automação'"
      :items="infoBlockItems"
      :content="infoBlockContent"
    />
    <section class="testimonials">
      <h2>Depoimentos</h2>
      <div class="testimonial" v-for="t in testimonials" :key="t.name">
        <blockquote>{{ t.content }}</blockquote>
        <cite>— {{ t.name }}</cite>
      </div>
    </section>

    <section class="benefits">
      <h2>Por que escolher a GHJ?</h2>
      <ul>
        <li v-for="b in benefits" :key="b">{{ b }}</li>
      </ul>
    </section>

    <section class="call-to-action">
      <h2>Fale com um especialista</h2>
      <p>
        Entre em contato agora e descubra como podemos ajudar sua empresa a crescer com automação.
      </p>
      <a href="/contact" class="contact-btn">Entrar em Contato</a>
    </section>
  </div>
</template>
