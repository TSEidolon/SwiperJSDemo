<template>
  <div class="swiper-container-main">
      
    <swiper 
      :effect="'coverflow'"
      :grabCursor="true"
      :centeredSlides="true"
      :coverflowEffect="{
        rotate: 50,
        stretch: 0,
        depth: 200,
        modifier: 1,
        slideShadows: false,
      }"

      :loop="true"
      :slidesPerView="3"
      :spaceBetween="30"
      
      :pagination="{
        clickable: true,
      }"
      :navigation="true"
      :modules="modules"
      class="mySwiper"
    >

      <swiper-slide>
        <div class="card-content">
          <span></span>
          <p>Text 1</p>
          <button>Click me</button>
        </div>
        
      </swiper-slide>


      <swiper-slide>Slide 2</swiper-slide>
      <swiper-slide>Slide 3</swiper-slide>
      <swiper-slide>Slide 4</swiper-slide>
      <swiper-slide>Slide 5</swiper-slide>
      <swiper-slide>Slide 6</swiper-slide>
      <swiper-slide>Slide 7</swiper-slide>
      <swiper-slide>Slide 8</swiper-slide>
      <swiper-slide>Slide 9</swiper-slide>
    </swiper>
  </div>
</template>

<script>


// Import Swiper Vue.js components

import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";
import "swiper/css/pagination";
import "swiper/css/effect-coverflow";
import "swiper/css/navigation";

// import required modules
import { Pagination, Navigation, EffectCoverflow } from "swiper";

export default {
  components: {
    Swiper,
    SwiperSlide,
 
  },
  setup() {
    return {
      modules: [Pagination, Navigation, EffectCoverflow],
    };
  },
};
</script>
<style>

/* .swiper-container-main {
  height: 100vh;
} */


.swiper-container-main {
  /* position: relative;
  height: 100%;

  background: #eee;
  
  color: #000;
  margin: 0;
  padding: 0; */
  position: relative;  
  background-color: black;
  padding: 3rem 0rem;

  width: 100%;
  display: flex;
  align-items: center;
}

.swiper {
  width: 100%;
  height: 1000px;
  padding: 40px 10px;
  background-color: grey;
  justify-content: center;
}




.swiper-slide {
  border-radius: 1rem;
  margin: 0;
  padding: 0;

  text-align: center;
  font-size: 18px;
  background: #fff;
  height: 100%;




  /* Center slide text vertically */
  display: -webkit-box;
  display: -ms-flexbox;
  display: -webkit-flex;
  display: flex;
  -webkit-box-pack: center;
  -ms-flex-pack: center;
  -webkit-justify-content: center;
  justify-content: center;
  -webkit-box-align: center;
  -ms-flex-align: center;
  -webkit-align-items: center;
  align-items: center;
}

.swiper-slide:hover {
  box-shadow: 0 3rem 6rem rgba(0, 0, 0, 0.4);
}

/* .swiper-slide::after {
  background-color: rgb(141, 141, 219);
  content: "";
  height: calc(100% + 3px);
  position: absolute;
  right: -7px;
  top: -9px;
  transition: background-color 300ms ease-in;
  width: 100%;
  z-index: -1;
} */
 

.swiper-slide img {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: contain;
}

.card-content {
  display: flex;
  flex-direction: column; 
  align-items: center;
 
  padding: 10px;
  position: relative;
  z-index: 100;
  height: 100%;
  width: 100%;
}

.card-content button {
  display: block;
  width: 50%;
  padding: 0.2rem;
  font-size: 1.8rem;
  text-align: center;
  /* background-color: var(--tertiary-color);
  color: var(--primary-color); */
  border-radius: 1rem;
  transition: all .2s ease-out;

  
}

.card-content button:hover {
  transform: translateY(-5%)
}



.swiper-pagination{
  position: absolute;
}

.swiper-pagination-bullet{
  height: 7px;
  width: 26px;
  border-radius: 25px;
  background: #7d2ae8;
}

.swiper-button-next, .swiper-button-prev{
  opacity: 0.7;
  color: #7d2ae8;
  transition: all 0.3s ease;
}
.swiper-button-next:hover, .swiper-button-prev:hover{
  opacity: 1;
  color: #7d2ae8;
}



</style>