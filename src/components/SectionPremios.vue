<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import "swiper/css";
import { Navigation } from "swiper/modules";


 const images = ["https://fakeimg.pl/340x340/", 
                 "https://fakeimg.pl/340x340/",
                 "https://fakeimg.pl/340x340/", 
                 "https://fakeimg.pl/340x340/", 
                 "https://fakeimg.pl/340x340/"];

const breakpointSlide = {   
  748: { slidesPerView: 2, spaceBetween:12 },  
  1134: { slidesPerView: 3, spaceBetween:12 }, 
  1520: { slidesPerView: 4, spaceBetween:12 },
}


</script>



<template>
    <section class="section__premios">
        <div>
            <h1 class="section__premio__h2">PRÊMIOS</h1>
        </div>
        <div>
            <Swiper 
                :space-between="12"
                @swiper="onSwiper"
                navigation
                loop
                :breakpoints="breakpointSlide"
                :modules="Navigation"
                class="swiper">
                
                <SwiperSlide v-for="image in images" :key="image" class="default-slider">
                    <img :src="image" alt="">
                </SwiperSlide>
            </Swiper>
        </div>
    </section>
</template>

<style scoped>


.section__premios{
    display: flex;
    align-items: center;
    flex-direction: column;
    margin-top: 11rem;
}

.swiper-horizontal{
    width: 1520px;
    margin-top: 12rem;
}

.section__premio__h2{
    color: black;
}

.default-slider{
    width: 100%;
}


@media (max-width:1519px){
    .swiper-horizontal{
        width: 1134px;
    }
}


@media (max-width:1133px){
    .swiper-horizontal{
        width: 748px;
    }
}

@media (max-width:747px){
    .swiper-horizontal{
        width: 601px;
    }
    
}


@media (max-width: 600px){

    .swiper-horizontal{
        width: 350px;
    }
}


@media (max-width:300px){
    .swiper-horizontal{
        width: 220px;
    }
    img{
        width: 220px;
    }
}


</style>