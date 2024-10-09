

<template>
  <section class="section__cadastrar">
    <div class="section__cadastrar__image">
      <img src="https://fakeimg.pl/500x400/">
    </div>
    <div class="section__cadastrar__button">
      <button type="button" class="button__cadastrar">
        CADASTRAR-SE
      </button>
    </div>
  </section>
</template>

<style scoped>

.section__cadastrar{
  display: grid;
  grid-template-columns: repeat(8,1fr);
  grid-template-rows: auto;
  row-gap: 6rem;
  width: 80%;
  margin-top: 100px;
}
.section__cadastrar__button{
  display: flex;
  justify-content: center;
  grid-column: 3 / span 4;
  
}

.section__cadastrar__image{
  display: flex;
  justify-content: center;
  margin-top: 150px;
  grid-column: 3 / span 4;
  
}

.button__cadastrar{
  border-radius: 48px;
  width: 100%;
}

@media (max-width: 1024px){
  .section__cadastrar__image{
    width: 250px;
    margin-top: 250px;
  }
  
}

</style>