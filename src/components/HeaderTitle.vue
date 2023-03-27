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
  <div class="header" v-if="reverseProps === false">
    <p class="text-xl text-xl--md">{{ subHeaderProps }}</p>
    <h3>{{ headerProps }}</h3>
  </div>

  <div class="header" v-else>
    <h3>{{ headerProps }}</h3>
    <p class="text-xl text-xl--md">{{ subHeaderProps }}</p>
  </div>
</template>

<style lang="scss" scoped>
@import '../assets/scss/styles.scss';

.header {
  display: flex;
  flex-direction: column;
  gap: toRem(8);
  text-align: center;
  align-items: center;
  justify-content: center;

  p {
    color: $p100;
  }
}
</style>
