<template>
  <div class="row app-download-row">
    <div class="container is-card is-background-white">
      <a href="#">
        <div class="bg-img"></div>
        <span>Shop Better, download the Platt App today</span>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: "AppDownload",
  props: {},
};
</script>

<style scoped lang="scss">
.app-download-row {
  padding-bottom: 1.5rem;
  a {
    width: 100%;
  }
  .bg-img {
    height: 10rem;
    background-repeat: no-repeat;
    background-position: right;
    background-size: auto 100%;
    background-image: url("/assets/panel/app-get-banner.png");
  }
  span {
    display: block;
    text-align: center;
    width: 100%;
    padding: 1rem 0;
    font-size: 1.2rem;
    font-weight: 500;
  }
}
@media (min-width: 850px), (max-width: 1023px) {
  .app-download-row {
    .bg-img {
      padding-bottom: 2rem;
    }
  }
}
@media (min-width: 1023px) {
  .app-download-row {
    grid-row: 6;
    grid-column: 1 / 5;
    padding: 0;
    margin: 1.5rem;
    margin-top: 0;
    .bg-img {
      width: 100%;
      height: auto;
      padding-bottom: 12rem;
    }
  }
}
@media (min-width: 1500px) {
  .app-download-row {
    .bg-img {
      padding-bottom: 20rem;
    }
  }
}
</style>
