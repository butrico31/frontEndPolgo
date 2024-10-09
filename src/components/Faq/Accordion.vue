<script setup>
    import { ref } from "vue";
    import SlideUpDown from "vue-slide-up-down";

    const props = defineProps({
        duvida: {
            type : Object,
            required : true,
        },
    });

    const visible = ref(false);

    function handleToggleAccordionVisible(){
        visible.value = !visible.value;
    }
</script>

<template>
  <section class="section__accordion">
    <div class="component__accordion">
      <div @click="handleToggleAccordionVisible" class="accordion__header">
        <div>
          <span class="accordion__title">{{ duvida.label }}</span>
        </div>
        <div class="accordion__icon">
          <div class="accordion__line"></div>
          <div
            class="accordion__line accordion__line__vertical"
            :class="{ 'accordion__line__vertical__active': visible }"
          ></div>
        </div>
      </div>
      <div>
      <slide-up-down :active="visible" class="wobbly__accordion" :duration="300">
        <div class="accordion__content" v-html="duvida.conteudo"></div>
      </slide-up-down>
      </div>
    </div>
  </section>
</template>

<style scoped>

.section__accordion{
  display: flex;
  justify-content: center;
}

.component__accordion {
  width: 1520px;
  display: flex;
  background-color: #ff8a84;
  border-radius: 25px;
  padding-inline: 25px;
  flex-direction: column;
}

.componente__accordion:last-child {
  border-bottom: none;
}

.accordion__header {
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding-block: 1.5rem;
}

.accordion__title {
  font-size: 1.25rem;
  font-weight: 700;
  pointer-events: none;
  color: #000;
}

.accordion__icon {
  width: 1.5rem;
  height: 1.5rem;
  border: 2px solid #000000;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
  pointer-events: none;
}

.accordion__line {
  width: 0.75rem;
  height: 2px;
  border-radius: 1px;
  background: #000000;
}

.accordion__line__vertical {
  position: absolute;
  transform: rotate(90deg);
  transition: transform 0.4s;
}

.accordion__line__vertical__active {
  transform: rotate(180deg);
}

.wobbly__accordion {
  transition-timing-function: ease-in-out;
}

.accordion__content {
  padding-bottom: 1.5rem;
  color: #000;
}
</style>