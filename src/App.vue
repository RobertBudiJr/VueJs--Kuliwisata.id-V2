<script setup>
import NavbarTop from './components/NavbarTop.vue';
import HeroSection from './sections/HeroSection.vue';
import SponsorSection from './sections/SponsorSection.vue';
import RecSection from './sections/RecSection.vue';
import NewsSection from './sections/NewsSection.vue';
</script>

<template>
  <NavbarTop></NavbarTop>
  <HeroSection></HeroSection>
  <SponsorSection></SponsorSection>
  <RecSection></RecSection>
  <NewsSection></NewsSection>
</template>

<style lang="scss" scoped>
@import './assets/scss/styles.scss';
</style>
