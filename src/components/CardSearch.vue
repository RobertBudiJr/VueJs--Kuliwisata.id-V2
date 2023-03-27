<script setup>
defineProps(['badgeProps', 'titleProps', 'locateProps', 'imgProps']);
</script>

<template>
  <div class="col-lg-3 col-md-6 col-sm-12">
    <div class="card card-search">
      <img :src="imgProps" class="card-img-top card-img-search" alt="" />
      <span class="badge rounded-pill text-sm card-badge-search">{{ badgeProps }}</span>
      <div class="card-body">
        <h4 class="card-title card-title-search">{{ titleProps }}</h4>
        <p class="card-text card-locate-search">{{ locateProps }}</p>
        <a href="#" class="btn btn--primary btn-card-search">Learn More</a>
      </div>
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
  padding: toRem(16);
  display: flex;
  flex-direction: column;
  gap: toRem(16);
  position: relative;
  box-shadow: rgba(0, 0, 0, 0.08) 0px 4px 12px;

  .card-img-search {
    // max-width: 257px;
    // max-height: 190px;
  }

  .card-badge-search {
    background: $p50;
    opacity: 0.6;
    color: $p500;
    width: fit-content;
    position: absolute;
    top: toRem(32);
    left: toRem(32);
  }

  .card-body {
    padding: 0;
    display: flex;
    flex-direction: column;
    text-align: center;
    align-items: center;
    justify-content: center;

    .card-locate-search {
      color: $ntr300;
    }

    .btn-card-search {
      width: 100%;
      margin-top: toRem(16);
    }
  }
}
</style>
