<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
    <div class="container container-fluid">
      <a href="#" class="navbar-brand">
        <img src="../assets/img/Logo.svg" alt="" />
      </a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse align-items-center justify-content-center" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item">
            <a class="nav-link active btn btn--tertiary btn--lg" aria-current="page" href="#">Home</a>
          </li>
          <li class="nav-item">
            <a class="nav-link btn btn--tertiary btn--lg" href="#">Places</a>
          </li>
          <li class="nav-item">
            <a class="nav-link btn btn--tertiary btn--lg" href="#">Culinary</a>
          </li>
          <li class="nav-item">
            <a class="nav-link btn btn--tertiary btn--lg" href="#">About Us</a>
          </li>
        </ul>
      </div>
      <form class="d-flex">
        <button class="btn btn--secondary btn--lg" type="submit">Register</button>
        <button class="btn btn--tertiary btn--lg" type="submit">Login</button>
      </form>
    </div>
  </nav>
</template>
<style lang="scss" scoped>
@import '../assets/scss/styles.scss';
.navbar {
  padding: 0;
  height: 67px;
  background-color: unset !important;
  margin-top: toRem(50);

  .navbar-brand {
    padding: 0;
    margin: 0;
  }

  .navbar-nav {
    gap: toRem(24);

    .nav-item {
      .nav-link {
        padding: toRem(20);
        color: $ntr100;

        &:hover {
          color: $p400;
        }

        &.active {
          color: $p300;
        }
      }
    }

    .d-flex {
      gap: toRem(16);
    }
  }
}
</style>
