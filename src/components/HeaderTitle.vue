<script setup>
defineProps({
  subHeaderProps: String,
  headerProps: String,
  reverseProps: {
    default: false,
  },
});
</script>

<template>
  <div class="flex-column header" v-if="reverseProps === false">
    <p class="text-xl text-xl--md">{{ subHeaderProps }}</p>
    <h3>{{ headerProps }}</h3>
  </div>

  <div class="flex-column header" v-else>
    <h3>{{ headerProps }}</h3>
    <p class="text-xl text-xl--md">{{ subHeaderProps }}</p>
  </div>
</template>

<style lang="scss" scoped>
@import '../assets/scss/styles.scss';

.header {
  gap: toRem(8);
  text-align: center;

  p {
    color: $p100;
  }
}
</style>
