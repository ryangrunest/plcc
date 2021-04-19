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
    }
    .card-content {
      // overflow-x: scroll;
      a {
        display: inline-block;
      }
    }
  }
}
</style>
