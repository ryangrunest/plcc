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
</style>
