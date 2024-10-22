<template>
  <section>
    <NavbarVue class="mb-4" />
    <HeaderSwiperVue class="mb-4" />
    <SetupStandVue />
    <AboutUs />
  </section>
</template>

<script setup>
// import { RouterLink } from 'vue-router'
import NavbarVue from '@/components/NavbarModel.vue'
import HeaderSwiperVue from '@/components/HeaderSwiper.vue'
import SetupStandVue from '@/components/SetupStand.vue'
import AboutUs from '@/components/AboutUs.vue'
</script>