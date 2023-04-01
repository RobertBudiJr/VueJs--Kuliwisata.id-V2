<script setup>
import { ref } from 'vue';
import HeaderTitle from '../components/HeaderTitle.vue';
import CarouselSwiper from '../components/CarouselSwiper.vue';
</script>

<template>
  <!-- Start Popular Section -->
  <section class="pops">
    <div class="container container--gen">
      <!-- Header -->
      <HeaderTitle headerProps="Hot Food of The Month" subHeaderProps="We recommend you the best culinary delights every time, let's taste the local flavor" reverseProps="true" />
      <!-- Content -->
      <CarouselSwiper />
      <a href="#" class="btn btn--primary btn-card-search" v-motion-pop-visible-once>Explore More</a>
    </div>
  </section>
  <!-- End Popular Section -->
</template>

<style lang="scss" scoped>
@import '../assets/scss/styles.scss';

section.pops {
  .container {
    gap: toRem(32);
  }
}
</style>
