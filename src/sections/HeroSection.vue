<script setup></script>

<template>
  <!-- Start Hero Section -->
  <section class="hero">
    <div class="container container--gen">
      <!-- Hero Header -->
      <div class="hero__header">
        <h1>
          Looking for
          <div class="word-translate">
            <span>Places?</span>
            <span>Foods?</span>
            <span>Drinks?</span>
          </div>
        </h1>
      </div>
      <!-- Hero Form -->
      <div class="hero__form input-group mb-3"><input type="text" class="form-control form-control-lg" placeholder="Pura Ulun" aria-label="SearchBar" aria-describedby="searchButton" /><span id="searchButton" class="search"></span></div>
      <!-- Gradient -->
      <div class="gradient-white"></div>
    </div>
  </section>
  <!-- End Hero Section -->
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
    gap: toRem(16);
    animation: fadeIn 0.4s ease-in;

    .gradient-white {
      position: absolute;
      width: 100%;
      height: 64px;
      bottom: 0;
      background-image: linear-gradient(180deg, transparent, $ntr0);
    }

    .hero__header {
      display: flex;
      word-break: normal;
      max-width: 625px;
      width: inherit;
      min-width: auto;

      @include media-breakpoint-down(md) {
        padding-inline: toRem(106);
        text-align: center;
      }

      @include media-breakpoint-down(sm) {
        padding-inline: 0;
      }

      @include media-breakpoint-down(xs-2) {
        padding-right: toRem(170);
      }

      h1 {
        text-align: justify;
        word-break: normal;
        color: $p50;
        position: relative;
        width: inherit;
        .word-translate {
          color: $ntr500;
          display: inline;
          text-indent: toRem(10);
          width: 260px;

          span {
            position: absolute;
            opacity: 0;
            overflow: hidden;
            -webkit-animation: rotateWord 10s linear infinite 0s;
            -ms-animation: rotateWord 10s linear infinite 0s;
            animation: rotateWord 10s linear infinite 0s;

            &:nth-child(2) {
              -webkit-animation-delay: 3s;
              -ms-animation-delay: 3s;
              animation-delay: 3s;
            }

            &:nth-child(3) {
              -webkit-animation-delay: 6s;
              -ms-animation-delay: 6s;
              animation-delay: 6s;
            }
          }
        }
      }
    }

    .hero__form {
      max-width: 625px;
      position: relative;
      border-radius: toRem(8);
      overflow: hidden;

      @include media-breakpoint-down(md) {
        padding-inline: toRem(4);
      }

      @include media-breakpoint-down(sm) {
        padding-inline: 0;
      }

      .form-control {
        border-top-right-radius: toRem(8);
        padding: toRem(12) toRem(24);
        padding-right: toRem(32);
        z-index: 1;

        &::placeholder {
          color: $ntr100;
        }
      }

      .search {
        position: absolute;
        z-index: 2;
        width: 24px;
        height: 24px;
        background-image: url(../assets/img/icons/search.svg);
        background-size: cover;
        right: 12px;
        top: 0;
        bottom: 0;
        margin: auto 0;
        cursor: pointer;

        // Override unecessary settings
        .input-group > :not(:first-child):not(.dropdown-menu):not(.valid-tooltip):not(.valid-feedback):not(.invalid-tooltip):not(.invalid-feedback) {
          margin-left: 0;
          border-top-left-radius: none;
          border-bottom-left-radius: none;
        }
      }
    }
  }
}
</style>
