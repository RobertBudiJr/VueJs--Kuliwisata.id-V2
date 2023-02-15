<script setup>
import NavbarTop from '../components/NavbarTop.vue';
</script>

<template>
  <section class="hero">
    <navbar-top></navbar-top>
    <div class="container">
      <h1>
        Looking for
        <div class="word-translate">
          <span>Places?</span>
          <span>Foods?</span>
          <span>Drinks?</span>
        </div>
      </h1>
      <input class="form-control me-2" type="search" placeholder="Pura Ulun" aria-label="Search" />
      <div class="gradient-white"></div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@import '../assets/scss/styles.scss';
section.hero {
  padding: toRem(50) 0;
  display: flex;
  flex-direction: column;
  gap: toRem(50);
  .container {
    background-image: url(../assets/img/hero-image.png);
    position: relative;
    background-size: cover;
    overflow: hidden;
    border-radius: toRem(20);
    height: 583px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: toRem(16);

    .gradient-white {
      position: absolute;
      width: 100%;
      height: 64px;
      bottom: 0;
      background-image: linear-gradient(180deg, transparent, $ntr0);
    }

    h1 {
      color: $p50;
      .word-translate {
        position: relative;
      }
    }
  }
}
</style>
