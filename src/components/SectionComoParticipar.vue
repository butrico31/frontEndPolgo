<script setup>
    const images = ["https://fakeimg.pl/362x362/","https://fakeimg.pl/362x362/","https://fakeimg.pl/362x362/","https://fakeimg.pl/362x362/"]
</script>

<template>
    <section class="section__comoParticipar">
        <div>
            <h1 class="section__comoParticipar__h1">COMO PARTICIPAR</h1>
        </div>
        <div class="section__comoParticipar__images">
            <div v-for="image in images" :key="image">
                <img :src="image" alt="" class="img__comoParticipar" >
            </div>
        </div>
        <div>
            <button type="button" class="button__cadastrar">
                CADASTRAR-SE
            </button>
        </div>
    </section>
</template>

<style scoped>
.section__comoParticipar{
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-top: 8rem;
}

.section__comoParticipar__h1{
    color: black;
}

.section__comoParticipar__images{
    display: flex;
    justify-content: center;
    flex-direction: row;
    flex-wrap: wrap;
    gap: 24px;
    margin-top: 11rem;
    width: auto;
}

.button__cadastrar{
  border-radius: 48px;
  width: 100%;
  margin-top: 12rem;
  padding-inline: 18rem;
}

</style>