<script setup>
import { ref } from 'vue';
import HeaderTitle from '../components/HeaderTitle.vue';
import CardSearch from '../components/CardSearch.vue';
import cardImg1 from '../assets/img/card-1.svg';
import cardImg2 from '../assets/img/card-2.svg';
import cardImg3 from '../assets/img/card-3.svg';
import cardImg4 from '../assets/img/card-4.svg';

const cardList = ref([
  {
    badgeProps: 'Island',
    imgProps: cardImg1,
    titleProps: 'Nusa Penida',
    locateProps: 'Bali, Indonesia.',
  },
  {
    badgeProps: 'Religion',
    imgProps: cardImg2,
    titleProps: 'Ulun',
    locateProps: 'Bali, Indonesia.',
  },
  {
    badgeProps: 'Beach',
    imgProps: cardImg3,
    titleProps: 'Kuta',
    locateProps: 'Bali, Indonesia.',
  },
  {
    badgeProps: 'Beach',
    imgProps: cardImg4,
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
      <div class="row g-1">
        <CardSearch v-for="items in cardList" v-bind:key="items.id" :badgeProps="items.badgeProps" :imgProps="items.imgProps" :titleProps="items.titleProps" :locateProps="items.locateProps"></CardSearch>
      </div>
    </div>
  </section>
  <!-- End Recommendation Section -->
</template>

<style lang="scss" scoped>
@import '../assets/scss/styles.scss';

section.rec {
  .row {
    --bs-gutter-x: 28px;
    --bs-gutter-y: 28px;
    // align-items: center;
    justify-content: center;
  }
}
</style>
