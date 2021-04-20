<template>
  <div class="row recently-viewed-row">
    <div class="container is-card">
      <div class="row card-header">
        <div class="column">
          <span>Recently Viewed</span>
        </div>
        <div class="column">
          <a class="is-text-green" href="#">View All</a>
        </div>
      </div>
      <div class="row card-content">
        <a href="#"><img src="@/assets/recent/11.png" alt="recent photo" /></a>
        <a href="#"><img src="@/assets/recent/22.png" alt="recent photo" /></a>
        <a href="#"><img src="@/assets/recent/22.png" alt="recent photo" /></a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Recents",
  props: {},
};
</script>

<style scoped lang="scss">
.recently-viewed-row {
  .row {
    width: 100%;
  }
  .is-card {
    padding: 1rem;
    background-color: var(--white);
    .card-header {
      width: 100%;
      padding: 0;
      * {
        font-size: 1.3rem;
        font-weight: 500;
      }
    }
    .card-content {
      a {
        display: inline-block;
      }
    }
  }
}
@media (min-width: 1023px) {
  .recently-viewed-row {
    grid-row: 4;
    grid-column: 3 / 5;
    padding: 0;
    margin-right: 1.5rem;
    height: 15rem;
    .container {
      padding: 0 2rem;
      justify-content: space-between;
      .card-header {
        width: calc(100% - 2rem);
        padding-top: 1.5rem;
        padding-bottom: 0;
      }
      .card-content {
        padding: 0;
        flex-grow: 1;
        a {
          width: 30%;
          max-width: 10rem;
          img {
            width: 100%;
          }
        }
      }
    }
  }
}
</style>
