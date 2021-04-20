<template>
  <div class="row deals-row">
    <a class="is-card" href="#"
      ><img src="@/assets/panel/deal.png" alt="todays deals"
    /></a>
  </div>
</template>

<script>
export default {
  name: "Deals",
  props: {},
};
</script>

<style scoped lang="scss">
.deals-row {
  a {
    width: 100%;
    height: auto;
    img {
      width: 100%;
      height: auto;
    }
  }
}
@media (min-width: 1023px) {
  .deals-row {
    grid-column: 1 / 3;
    grid-row: 4;
    padding: 0;
    margin-left: 1.5rem;
    a {
      img {
        height: 15rem;
      }
    }
  }
}
</style>
