<script setup>
import Navbar from './components/Navbar.vue'
import Hero from './components/Hero.vue'
import Sobre from './components/Sobre.vue'
import Projetos from './components/Projetos.vue'
import Contato from './components/Contato.vue'
import Skills from './components/Skills.vue'
import Footer from './components/Footer.vue'
import Formacao from './components/Formacao.vue'
import { onMounted } from 'vue'
onMounted(() => {
  if (!document.querySelector('link[href*="devicon"]')) {
    const link = document.createElement('link')
    link.rel = 'stylesheet'
    link.href = 'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/devicon.min.css'
    document.head.appendChild(link)
  }
})
</script>
<template>
  <Navbar />
<main>
  <Hero />
  <Projetos />
  <Skills />
  <Sobre />
  <Formacao />
  <Contato />
</main>

<Footer />
</template>
<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
  overflow-x: hidden;
}

body {
  font-family: 'Poppins', sans-serif;
  background: #0F172A;
  color: white;
  overflow-x: hidden;
  min-width: 320px;
}

main {
  width: 100%;
  max-width: 100%;
  padding-top: 80px; /* compensar navbar fixa */
  overflow-x: hidden;
}

/* Tablets */
@media (max-width: 768px) {
  main {
    padding-top: 70px;
  }
}

/* Celulares */
@media (max-width: 480px) {
  main {
    padding-top: 65px;
  }
}
</style>