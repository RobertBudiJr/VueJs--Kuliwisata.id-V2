<script setup></script>

<template>
  <!-- Start News Section -->
  <section class="news">
    <div class="container container--gen" v-motion-slide-visible-bottom>
      <div class="flex-column wrapper">
        <div class="flex-column news__header">
          <h3>Subscibe to Our Newsletter</h3>
          <p class="text-l">Get weekly update about our recommendation on your email, no spam guaranteed we promise ✌️</p>
        </div>
        <div class="flex-row news__form">
          <input class="form-control form-control-lg" type="text" placeholder="xxxx@gmail.com" />
          <span class="mail"></span>
          <button class="btn btn--primary btn--lg">Subscribe</button>
        </div>
      </div>
    </div>
  </section>
  <!-- End News Section -->
</template>

<style lang="scss" scoped>
@import '../assets/scss/styles.scss';

section.news {
  .container {
    @include media-breakpoint-down(sm) {
      background: $p75;
    }
  }
  .wrapper {
    background: $p75;
    border-radius: toRem(8);
    overflow: hidden;
    width: 100%;
    gap: toRem(32);
    padding: toRem(64);

    @include media-breakpoint-down(sm) {
      padding: toRem(24);
      gap: toRem(16);
    }

    .news__header {
      text-align: center;
      gap: toRem(8);

      h3 {
        color: $ntr0;
      }
    }

    .news__form {
      width: 100%;
      gap: toRem(16);
      position: relative;

      @include media-breakpoint-down(md) {
        flex-wrap: wrap;
      }

      .form-control {
        padding-left: toRem(64);

        &::placeholder {
          color: $ntr100;
        }
      }

      .mail {
        position: absolute;
        width: 24px;
        height: 24px;
        background-image: url(../assets/img/icons/mail.svg);
        background-size: cover;
        left: 24px;
        top: 0;
        bottom: 0;
        margin: auto 0;

        @include media-breakpoint-down(md) {
          top: 12px;
          bottom: unset;
        }
      }

      .btn {
        @include media-breakpoint-down(md) {
          width: 100%;
        }
      }
    }
  }
}
</style>
