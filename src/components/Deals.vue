<template>
  <row class="deals-row">
    <a class="is-card" href="#"
      ><img src="@/assets/panel/deal.png" alt="todays deals"
    /></a>
  </row>
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
