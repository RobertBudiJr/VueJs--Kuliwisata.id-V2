<script setup></script>

<template>
  <!-- Start Footer Section -->
  <footer class="footer">
    <div class="container container--gen flex-row container--footer">
      <div class="flex-column footer__wrapper" v-motion-fade-visible-once>
        <div class="footer__logo"></div>
        <p class="text-sm footer__desc">Kuliwisata is a web platform that provides assistance in obtaining popular information about interesting places and delicious culinary delights throughout Indonesia.</p>
      </div>

      <div class="flex-column footer__wrapper" v-motion-fade-visible-once>
        <p class="text-xl text-xl--lg">Pages</p>
        <ul class="footer__menus">
          <li><a href="#">Home</a></li>
          <li><a href="#">Places</a></li>
          <li><a href="#">Culinary</a></li>
          <li><a href="#">About Us</a></li>
        </ul>
      </div>

      <div class="flex-column footer__wrapper" v-motion-fade-visible-once>
        <p class="text-xl text-xl--lg">Service</p>
        <ul class="footer__menus">
          <li><a href="#">Information</a></li>
          <li><a href="#">Maps</a></li>
        </ul>
      </div>

      <div class="flex-column footer__wrapper" v-motion-fade-visible-once>
        <p class="text-xl text-xl--lg">Contact</p>
        <ul class="footer__menus">
          <li>
            <a href="#"><span class="icon icon--phone"></span>(406) 555-0120</a>
          </li>
          <li>
            <a href="#"><span class="icon icon--mail"></span>info@kuliwisata.id</a>
          </li>
          <li>
            <a href="#"><span class="icon icon--location"></span>Jl. Danau Ranau, Sawojajar, Kec. Kedungkandang, Kota Malang, Jawa Timur 65139</a>
          </li>
        </ul>
      </div>

      <div class="flex-column footer__wrapper" v-motion-fade-visible-once>
        <p class="text-xl text-xl--lg">Sosial media</p>
        <ul class="flex-row footer__menus">
          <li>
            <a href="#" class="icon icon--facebook"></a>
          </li>
          <li>
            <a href="#" class="icon icon--twitter"></a>
          </li>
          <li>
            <a href="#" class="icon icon--linkedin"></a>
          </li>
          <li>
            <a href="#" class="icon icon--instagram"></a>
          </li>
        </ul>
      </div>
    </div>
  </footer>
  <!-- End News Section -->
</template>

<style lang="scss" scoped>
@import '../assets/scss/styles.scss';

footer.footer {
  background: $p500;
  color: $ntr0;

  .container--footer {
    @include media-breakpoint-down(md) {
      flex-direction: column;
      align-items: center;
      justify-content: center;
      gap: toRem(48);
      & > * {
        width: 100% !important;
        max-width: 100% !important;
        text-align: center;
      }
    }
  }
  .flex-row {
    justify-content: space-between;
    flex-wrap: wrap;
    align-items: flex-start;
  }

  .flex-column {
    align-items: flex-start;

    @include media-breakpoint-down(md) {
      align-items: center;
    }
  }

  .footer__wrapper {
    gap: toRem(32);

    & > ul {
      display: flex;
      flex-direction: column;
      gap: toRem(16);

      @include media-breakpoint-down(md) {
        align-items: center;
      }
    }

    & > ul li a {
      color: $ntr50;
      gap: toRem(16);

      &:hover {
        color: $p200;
      }
    }

    .icon {
      background-size: contain;
      background-repeat: no-repeat;
      background-position: center;
      width: 24px;
      aspect-ratio: 1 / 1;
      height: 26px;

      &--phone {
        background-image: url(../assets/img/icons/call.svg);
      }
      &--mail {
        background-image: url(../assets/img/icons/mail-white.svg);
      }
      &--location {
        background-image: url(../assets/img/icons/location.svg);
      }
      &--facebook {
        background-image: url(../assets/img/icons/facebook-logo.svg);

        &:hover {
          background-image: url(../assets/img/icons/facebook-logo-hover.svg);
        }
      }
      &--twitter {
        background-image: url(../assets/img/icons/twitter-logo.svg);

        &:hover {
          background-image: url(../assets/img/icons/twitter-logo-hover.svg);
        }
      }
      &--linkedin {
        background-image: url(../assets/img/icons/linkedin-logo.svg);

        &:hover {
          background-image: url(../assets/img/icons/linkedin-logo-hover.svg);
        }
      }
      &--instagram {
        background-image: url(../assets/img/icons/instagram-logo.svg);

        &:hover {
          background-image: url(../assets/img/icons/instagram-logo-hover.svg);
        }
      }
    }
  }
  .footer__wrapper:nth-child(1) {
    max-width: 200px;

    .footer__logo {
      background-image: url(../assets/img/logo-white.svg);
      background-size: cover;
      width: 70%;
      aspect-ratio: 6.38 / 1;

      @include media-breakpoint-down(md) {
        width: 50%;
      }
    }
  }

  .footer__wrapper:nth-child(4) {
    max-width: 250px;
  }
}
</style>
