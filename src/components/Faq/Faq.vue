<script setup>

import Accordion from './Accordion.vue'


const duvidas = [
    {
        label : "duvida 1",
        conteudo : "Lorem ipsum dolor sit amet, consectetur adipiscing elit."
    },
    {
        label : 'duvida 2',
        conteudo : 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.'
    },
    {
        label : 'duvida 3',
        conteudo : 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.'
    },
    {
        label : 'duvida 4',
        conteudo : 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.'
    },
    {
        label : 'duvida 5',
        conteudo : 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.'
    },
    {
        label : 'duvida 6',
        conteudo : 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.'
    },
];

</script>

<template>
    <section class="container">
        <div class="duvidas">
            <h1>Duvidas Frequentes</h1>
        </div>
        <div class="component__faq">
            <Accordion v-for="duvida in duvidas" :key="duvida.label" :duvida="duvida"></Accordion>
        </div>
    </section>
    
</template>

<style scoped>

.container{
    display: flex;
    flex-direction: column;
    width: 100%;
    align-items: center;
    margin-top: 12rem;
}

.duvidas{
    color: black;
    
}

.component__faq {
    width: 100%;
    background: transparent;
    margin-inline: auto;
    padding: 2rem;
    display: flex;
    flex-direction: column;
    gap: 3rem 0;
    margin-top: 11rem;
    
}

@media (max-width: 480px) {
  .component__faq {
    padding: 1.5rem;
  }
}
</style>