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

const infoBlockContent = `Na GHJ Automação, unimos eficiência e inovação para transformar processos industriais ou facilitar a sua rotina com soluções inteligentes. Nossa equipe é especializada em identificar oportunidades de melhoria, propor tecnologias adequadas e acompanhar a implantação de cada projeto do início ao fim. Conheça algumas das áreas em que podemos atuar, e caso esteja interessado, solicite uma consultoria gratuita nos campos abaixo:`

const testimonials = [
  { name: 'João S.', content: 'Profissionais incríveis e suporte impecável. Recomendo muito!' },
  { name: 'Empresa XYZ', content: 'Reduzimos 40% dos custos com as soluções da GHJ.' },
  { name: 'Maria A.', content: 'Me ajudaram a automatizar minha linha de produção com IoT!' }
]

const benefits = [
  'Atendimento personalizado',
  'Equipe multidisciplinar',
  'Uso de tecnologias emergentes',
  'Agilidade na entrega de projetos',
  'Consultoria gratuita inicial'
]
</script>

<template>
  <div class="container">
    <InfoBlock
      :title="'Soluções em Automação'"
      :items="infoBlockItems"
      :content="infoBlockContent"
    />

    <ConsultForm />

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
      <p>Entre em contato agora e descubra como podemos ajudar sua empresa a crescer com automação.</p>
      <a href="/contact" class="contact-btn">Entrar em Contato</a>
    </section>
  </div>
</template>

<style scoped>
.container {
  padding: 2rem 1rem;
  max-width: 800px;
  margin: auto;
}

section {
  margin-top: 3rem;
}

.testimonials h2,
.benefits h2,
.call-to-action h2 {
  font-size: 1.5rem;
  margin-bottom: 1rem;
  color: #42b983;
}

.testimonial {
  margin-bottom: 1.5rem;
  background: #f0f0f0;
  padding: 1rem;
  border-left: 4px solid #42b983;
  border-radius: 4px;
}

.dark .testimonial {
  background: #2d2d2d;
  color: #eee;
}

.benefits ul {
  list-style: disc inside;
  padding-left: 1rem;
}

.call-to-action {
  text-align: center;
  background: #e0ffe0;
  padding: 2rem;
  border-radius: 8px;
}

.dark .call-to-action {
  background: #1f1f1f;
  color: #fff;
}

.contact-btn {
  display: inline-block;
  margin-top: 1rem;
  padding: 0.75rem 1.5rem;
  background: #4281b9;
  color: white;
  border-radius: 4px;
  text-decoration: none;
}
</style>
