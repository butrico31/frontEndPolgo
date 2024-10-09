<script setup>
import Faq from './components/Faq/Faq.vue'
import Header from './components/Header.vue'
import SectionCadastro from './components/SectionCadastro.vue';
import SectionComoParticipar from './components/SectionComoParticipar.vue';
import SectionPremios from './components/SectionPremios.vue';
import Winners from './components/Winners/Winners.vue';
import Footer from './components/Footer.vue'
</script>

<template>
  <div class="App">
    <Header />
    <SectionCadastro />
    <SectionComoParticipar />
    <SectionPremios/> 
    <Faq />
    <Winners/>
    <Footer />
  </div>
</template>

<style scoped>
.App{
  display: flex;
  align-items: center;
  flex-direction: column;
}
</style>
