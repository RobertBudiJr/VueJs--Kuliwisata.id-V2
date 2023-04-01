<template>
  <div class="carousel-swipe">
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
        <img class="image-carousel" src="../assets/img/food-1.png" />
        <div class="hover-content" style="display: none">
          <h4>Sate Klathak</h4>
          <p class="text-md">
            Sate Klathak adalah makanan khas yang berasal dari Kabupaten Bantul berbahan dasar daging kambing. Dengan spesifikasi tusuk sate terbuat dari besi jeruji sepeda. Cara memasak dengan dibakar dan hanya diberi bumbu garam. Cara
            penghidangannya setiap porsi atau menu umumnya terdiri dari 2 tusuk sate sampai 4 tusuk.
          </p>
        </div>
      </swiper-slide>
      <swiper-slide class="slide">
        <img class="image-carousel" src="../assets/img/food-2.png" />
        <div class="hover-content" style="display: none">
          <h4>Ayam Betutu</h4>
          <p class="text-md">
            Betutu adalah lauk yang terbuat dari ayam atau bebek yang utuh yang berisi bumbu, kemudian dipanggang dalam api sekam. Betutu ini telah dikenal di seluruh kabupaten di Bali. Betutu merupakan jenis makanan tradisional daerah Bali
            yang bahan mentahnya berupa karkas utuh itik dan ayam. Kata betutu berasal dari kata tunu yang berarti bakar dan dirangkai dengan kata be yang berarti daging. Berdasarkan uraian tersebut betutu berarti daging yang dibakar. Ayam
            betutu merupakan jenis lauk pauk yang dibuat dari daging ayam yang telah dibersihkan kemudian dibalurkan bumbu khas Bali yang dikenal dengan base genep di seluruh permukaan tubuh daging ayam dan sebagian lagi dimasukkan ke dalam
            rongga abdomennya.
          </p>
        </div>
      </swiper-slide>
      <swiper-slide class="slide">
        <img class="image-carousel" src="../assets/img/food-3.png" />
        <div class="hover-content" style="display: none">
          <h4>Nasi Gandul</h4>
          <p class="text-md">
            Nasi Gandul adalah masakan khas yang berasal dari daerah Pati, Jawa Tengah, Indonesia yang sepintas mirip dengan Semur Daging dan Gulai. Nasi gandul sepintas mirip dengan perpaduan soto dan gule, berupa daging yang dengan kuah
            yang berwarna kecoklatan dengan rasa gurih manis.
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
