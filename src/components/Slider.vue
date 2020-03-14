<template>
  <swiper class="slider" :options="swiperOptions">
    <swiper-slide class="slider__slide" v-for="(slide, index) in swiperData" :key="index">
      <h2 class="slider__title">{{ slide.title }}</h2>
      <span class="slider__desc">{{ slide.desc }}</span>
      <button class="slider__read-more-btn brown-btn">Подбробнее</button>
      <div class="slider__counter counter">
        <span class="counter__current">{{
          (index + 1).toLocaleString("ru-RU", { minimumIntegerDigits: 2, useGrouping: false })
        }}</span>

        <span class="counter__total">/{{ swiperData.length }}</span>
      </div>
      <img class="slider__img" :src="slide.img" alt="специальное предложение" />
    </swiper-slide>
    <div class="slider__button-prev" slot="button-prev"></div>
    <div class="slider__button-next" slot="button-next"></div>
    <div class="slider__pagination" slot="pagination"></div>
  </swiper>
</template>

<script>
import "swiper/dist/css/swiper.css";
import { swiper, swiperSlide } from "vue-awesome-swiper";
export default {
  name: "Slider",
  components: {
    swiper,
    swiperSlide
  },
  data() {
    return {
      swiperOptions: {
        slidesPerView: "auto",
        spaceBetween: 32,
        slideActiveClass: "slider__slide_active",
        navigation: {
          nextEl: ".slider__button-next",
          prevEl: ".slider__button-prev"
        },
        pagination: {
          el: ".slider__pagination",
          dynamicBullets: true,
          clickable: true,
          bulletClass: "slider__bullet",
          bulletActiveClass: "slider__bullet_active"
        },
        breakpoints: {
          768: {
            slidesPerView: 1,
            spaceBetween: 0
          }
        }
      },
      // для теста:
      swiperData: [
        {
          title: "Классика в современном исполнении",
          desc: "Скидки до 70% на коллекцию NewDoors",
          img: `https://via.placeholder.com/1336x800`,
          link: "/"
        },
        {
          title: "Классика в современном исполнении",
          desc: "Скидки до 70% на коллекцию NewDoors",
          img: `https://via.placeholder.com/2672x1600`,
          link: "/"
        },
        {
          title: "Классика в современном исполнении",
          desc: "Скидки до 70% на коллекцию NewDoors",
          img: `https://via.placeholder.com/2672x1600`,
          link: "/"
        },
        {
          title: "Классика в современном исполнении",
          desc: "Скидки до 70% на коллекцию NewDoors",
          img: `https://via.placeholder.com/2672x1600`,
          link: "/"
        }
      ]
    };
  }
};
</script>
