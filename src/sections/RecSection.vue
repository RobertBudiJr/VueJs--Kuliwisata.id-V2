<script setup>
import { ref } from 'vue';
import HeaderTitle from '../components/HeaderTitle.vue';
import CardSearch from '../components/CardSearch.vue';
import cardImg1 from '../assets/img/card-1.png';
import cardImg2 from '../assets/img/card-2.png';
import cardImg3 from '../assets/img/card-3.png';
import cardImg4 from '../assets/img/card-4.png';

// V Lazy Image
import cardImg1Unload from '../assets/img/card-1-unload.png';
import cardImg2Unload from '../assets/img/card-2-unload.png';
import cardImg3Unload from '../assets/img/card-3-unload.png';
import cardImg4Unload from '../assets/img/card-4-unload.png';

const cardList = ref([
  {
    badgeProps: 'Island',
    imgProps: cardImg1,
    imgLoadProps: cardImg1Unload,
    titleProps: 'Nusa Penida',
    locateProps: 'Bali, Indonesia.',
  },
  {
    badgeProps: 'Religion',
    imgProps: cardImg2,
    imgLoadProps: cardImg2Unload,
    titleProps: 'Ulun',
    locateProps: 'Bali, Indonesia.',
  },
  {
    badgeProps: 'Beach',
    imgProps: cardImg3,
    imgLoadProps: cardImg3Unload,
    titleProps: 'Kuta',
    locateProps: 'Bali, Indonesia.',
  },
  {
    badgeProps: 'Beach',
    imgProps: cardImg4,
    imgLoadProps: cardImg4Unload,
    titleProps: 'Seminyak',
    locateProps: 'Bali, Indonesia.',
  },
]);
</script>

<template>
  <!-- Start Recommendation Section -->
  <section class="rec">
    <div class="container container--gen">
      <!-- Header -->
      <HeaderTitle subHeaderProps="Recommendation" headerProps="Most Searched Places" />
      <!-- Content -->
      <div class="row g-1 rec__content">
        <CardSearch v-for="items in cardList" v-bind:key="items.id" :badgeProps="items.badgeProps" :imgProps="items.imgProps" :titleProps="items.titleProps" :locateProps="items.locateProps"></CardSearch>
      </div>
    </div>
  </section>
  <!-- End Recommendation Section -->
</template>

<style lang="scss" scoped>
@import '../assets/scss/styles.scss';

section.rec {
  .rec__content {
    --bs-gutter-x: 28px;
    --bs-gutter-y: 28px;
    // align-items: center;
    justify-content: center;
  }
}
</style>
