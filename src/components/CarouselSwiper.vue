<template>
  <div class="carousel-swipe" v-motion-fade-visible-once>
    <swiper
      class="swiper"
      :modules="modules"
      :pagination="true"
      :effect="'coverflow'"
      :grab-cursor="true"
      :centered-slides="true"
      :slides-per-view="'auto'"
      :coverflow-effect="{
        rotate: 50,
        stretch: 0,
        depth: 100,
        modifier: 1,
        slideShadows: true,
      }"
    >
      <!-- <swiper-slide class="slide" v-for="items in carouselList" v-bind:key="items.id">
        <img class="image-carousel" :src="items.imgProps" />
        <div class="hover-content" style="display: none">
          <h4>{{ items.titleProps }}</h4>
          <p class="text-md">
            {{ items.descProps }}
          </p>
        </div>
      </swiper-slide> -->
      <swiper-slide class="slide">
        <img class="image-carousel" src="../assets/img/food-1.png" alt="Sate Klathak" />
        <div class="hover-content" style="display: none">
          <h4>Sate Klathak</h4>
          <p class="text-md">
            Sate Klathak is a specialty food originating from Bantul Regency made from mutton. With specifications of skewers made of iron bicycle spokes. The cooking method is grilled and only seasoned with salt. Each portion or menu
            generally consists of 2 skewers to 4 skewers.
          </p>
        </div>
      </swiper-slide>
      <swiper-slide class="slide">
        <img class="image-carousel" src="../assets/img/food-2.png" alt="Ayam Betutu" />
        <div class="hover-content" style="display: none">
          <h4>Ayam Betutu</h4>
          <p class="text-md">
            Betutu is a side dish made from a whole chicken or duck that is filled with spices, then roasted in a husk fire. Betutu is known throughout all regencies in Bali. Betutu is a type of traditional Balinese food whose raw
            ingredients are whole carcasses of duck and chicken. The word betutu comes from the word tunu which means grilled and is coupled with the word be which means meat. Based on this description, betutu means grilled meat. Chicken
            betutu is a type of side dish made from chicken meat that has been cleaned and then spread Balinese spices known as "base genep" over the entire surface of the chicken body and partly inserted into the abdominal cavity.
          </p>
        </div>
      </swiper-slide>
      <swiper-slide class="slide">
        <img class="image-carousel" src="../assets/img/food-3.png" alt="Nasi Gandul" />
        <div class="hover-content" style="display: none">
          <h4>Nasi Gandul</h4>
          <p class="text-md">
            Nasi Gandul is a specialty dish originating from Pati, Central Java, Indonesia that is similar to Semur Daging and Gulai. Nasi gandul is similar to a combination of soto and gule, in the form of meat in a brownish sauce with a
            sweet savory taste.
          </p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
import { ref } from 'vue';
import { defineComponent } from 'vue';
import { Pagination, EffectCoverflow } from 'swiper';
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/pagination';
import 'swiper/css/effect-coverflow';

export default defineComponent({
  name: 'swiper-example-3d-coverflow',
  title: '3D Coverflow effect',
  url: import.meta.url,
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [Pagination, EffectCoverflow],
    };
  },
});
</script>

<style lang="scss" scoped>
@import '../assets/scss/styles.scss';
.swiper {
  height: 100%;
  width: 100%;
  padding-bottom: 50px;
  .slide {
    position: relative;
    width: 800px;
    // height: 600px;
    aspect-ratio: 4 / 3;

    @include media-breakpoint-down(xl) {
      width: 600px;
    }

    @include media-breakpoint-down(sm) {
      width: 300px;
    }

    img {
      display: block;
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
    .hover-content {
      position: absolute;
      inset: 0;
      color: $ntr0;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      align-items: center;
      text-align: center;
      height: inherit;
      padding: toRem(32);
      background-color: rgb($ntr900, 0.4);
      border-radius: 8px;
      overflow: hidden;
      transition: background-color 0.5s;

      @include media-breakpoint-down(sm) {
        padding: toRem(16);
        justify-content: center;
      }

      p {
        @include media-breakpoint-down(sm) {
          display: none;
        }
      }
    }
  }

  .swiper-slide-active {
    &:hover {
      .hover-content {
        display: flex !important;
      }
    }
  }
}
</style>
