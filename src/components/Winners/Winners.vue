<script setup>
import Accordion from './Accordion.vue';
import { onMounted, ref } from 'vue';

onMounted(() => {
    fetchWinners();
});

const winners = ref([]);  
const groupedWinners = ref([]);  

const fetchWinners = async () => {
    try {
        const response = await fetch("https://backendpolgo.onrender.com/winners");
        const data = await response.json();
        winners.value = data;
        groupWinnersByDate();
    } catch (error) {
        console.error('Erro ao buscar ganhadores:', error);
    }
}

const groupWinnersByDate = () => {
    const grouped = winners.value.reduce((acc, winner) => {
        if (!acc[winner.date]) {
            acc[winner.date] = [];
        }
        acc[winner.date].push(winner);
        return acc;
    }, {});

    groupedWinners.value = Object.entries(grouped).map(([date, winners]) => ({ date, winners }));
};
</script>

<template>
    <section class="section__winners">
        <div>
            <h1 class="winners__h1">GANHADORES</h1>
        </div>
        <div class="component__winner">
            
            <Accordion v-for="(group, index) in groupedWinners" :key="group.date" :winner="group" :index="index"></Accordion>
        </div>
    </section>
</template>

<style scoped>


.component__winner {
    margin-top: 11rem;
    width: 100%;
    background: transparent;
    margin-inline: auto;
    padding: 2rem;
    display: flex;
    flex-direction: column;
    gap: 3rem 0;
}

.section__winners {
    width: 100%;
    margin-top: 12rem;
    display: flex;
    flex-direction: column;
    align-items: center; 
}

.winners__h1 {
    color: black;
}

@media (max-width: 480px) {
    .component__faq {
        padding: 1.5rem;
    }
}
</style>
