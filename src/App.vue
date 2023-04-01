<script setup>
import NavbarTop from './components/NavbarTop.vue';
import HeroSection from './sections/HeroSection.vue';
import SponsorSection from './sections/SponsorSection.vue';
import RecSection from './sections/RecSection.vue';
import NewsSection from './sections/NewsSection.vue';
import FooterSection from './sections/FooterSection.vue';
</script>

<template>
  <NavbarTop></NavbarTop>
  <HeroSection></HeroSection>
  <SponsorSection></SponsorSection>
  <RecSection></RecSection>
  <NewsSection></NewsSection>
  <FooterSection></FooterSection>
</template>

<style lang="scss" scoped>
@import './assets/scss/styles.scss';
</style>
