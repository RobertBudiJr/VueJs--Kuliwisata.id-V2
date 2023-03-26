<script setup>
import HeaderTitle from '../components/HeaderTitle.vue';
import { ref } from 'vue';
import sponsor1 from '../assets/img/sponsor-1.svg';
import sponsor2 from '../assets/img/sponsor-2.svg';
import sponsor3 from '../assets/img/sponsor-3.svg';
import sponsor4 from '../assets/img/sponsor-4.svg';

const sponsorList = ref([sponsor1, sponsor2, sponsor3, sponsor4]);
</script>

<template>
  <!-- Start Sponsor Section -->
  <section class="sponsor">
    <div class="container">
      <!-- Header -->
      <HeaderTitle
        subHeaderProps="Sponsored"
        headerProps="We are Supported by
Official Government Institutions"
        reverseProps="true"
      />
      <!-- Content -->
      <div class="row gy-1 sponsor-list">
        <img class="col-lg-3 col-md-6 col-sm-12" v-for="items in sponsorList" v-bind:key="items" :src="items" alt="" />
      </div>
    </div>
  </section>
  <!-- End Sponsor Section -->
</template>

<style lang="scss" scoped>
@import '../assets/scss/styles.scss';

section.sponsor {
  .container {
    display: flex;
    flex-direction: column;
    gap: toRem(32);
    align-items: center;
    justify-content: center;
    padding: toRem(80) 0;

    .sponsor-list {
      width: 100%;
      --bs-gutter-y: 24px;
      & > * {
        max-height: 80px;
        height: auto;
      }
    }
  }
}
</style>
