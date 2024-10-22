<template>
  <swiper
    :effect="'cards'"
    :grabCursor="true"
    :modules="modules"
    class="mySwiper px-4 overflow-hidden"
  >
    <template v-for="(item, index) in productList" :key="index">
      <swiper-slide class="p-3 paperDarkBg"
        ><div
          class="card paperDarkBg rounded-0 border-primary border-3 text-center"
        >
          <div class="card-body">
            <div class="cart-title h3 text-uppercase">
              {{ item.title }}
            </div>
            <div class="card-text h6">
              {{ item.describe }}
            </div>
          </div>
          <img :src="item.image" class="card-img-top px-5" alt="..." />
          <div class="card-body">
            <h6 class="card-text text-primary mb-4">
              {{ item.content }}
            </h6>
            <div class="text-center">
              <router-link to="/" class="btn btn-primary p-2 px-3">
                VIEW MORE
              </router-link>
            </div>
          </div>
        </div></swiper-slide
      >
    </template>
  </swiper>
</template>

<style scoped>
@import 'swiper/css/effect-cards';

.swiper-slide {
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 22px;
  font-weight: bold;
  color: #333;
}
</style>

<script setup>
import image1 from '@/assets/images/product1.jpg'
import image2 from '@/assets/images/product2.jpg'
import image3 from '@/assets/images/product3.jpeg'
import { ref } from 'vue'
import { RouterLink } from 'vue-router'
import { Swiper, SwiperSlide } from 'swiper/vue'
// import required modules
import { EffectCards } from 'swiper/modules'

const modules = ref([EffectCards])
const productList = ref([
  {
    image: image1,
    title: 'Rendang sapi',
    describe:
      'Aromanya yang masih melekat di mulut membuat orang tersenyum dan berkata: "Enak!"',
    content:
      'Minyak berwarna jingga cerah yang muncul dari campuran cabai, rempah-rempah, santan, dan lemak daging sapi melapisi setiap potongan daging sapi dengan segala bumbunya dengan lembut.',
  },
  {
    image: image2,
    title: 'Mie Ayam',
    describe:
      'Aromanya yang masih melekat di mulut membuat orang tersenyum dan berkata: "Enak!"',
    content:
      'Minyak berwarna jingga cerah yang muncul dari campuran cabai, rempah-rempah, santan, dan lemak daging sapi melapisi setiap potongan daging sapi dengan segala bumbunya dengan lembut.',
  },
  {
    image: image3,
    title: 'Bagelen',
    describe:
      'Aromanya yang masih melekat di mulut membuat orang tersenyum dan berkata: "Enak!"',
    content:
      'Minyak berwarna jingga cerah yang muncul dari campuran cabai, rempah-rempah, santan, dan lemak daging sapi melapisi setiap potongan daging sapi dengan segala bumbunya dengan lembut.',
  },
])
</script>
