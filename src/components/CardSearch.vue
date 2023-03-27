<script setup>
defineProps(['badgeProps', 'titleProps', 'locateProps', 'imgProps']);
</script>

<template>
  <div class="card col-lg-3 col-md-6 col-sm-12 card-search">
    <img :src="imgProps" class="card-img-top" alt="" />
    <span class="badge rounded-pill text-sm">{{ badgeProps }}</span>
    <div class="card-body">
      <h4 class="card-title">{{ titleProps }}</h4>
      <p class="card-text">{{ locateProps }}</p>
      <a href="#" class="btn btn--primary">Learn More</a>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import '../assets/scss/styles.scss';

.card-search {
  background: rgba(255, 255, 255, 0.4);
  border-radius: 8px;
  overflow: hidden;
  --bs-card-border-color: none;
}
</style>
