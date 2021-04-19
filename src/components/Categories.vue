<template>
  <div class="row is-background-white categories-container">
    <a href="#">
      <img src="@/assets/ic/black/ic_categories.png" alt="shopping icon" />
      <span>Shop All Categories</span>
      <img
        class="arrow-icon"
        src="@/assets/ic/black/ic_arrow_forward.png"
        alt="arrow icon"
    /></a>
  </div>
</template>

<script>
export default {
  name: "Categories",
  props: {},
};
</script>

<style scoped lang="scss">
.categories-container {
  padding: 2.2rem 2rem;
  position: relative;
  a {
    position: relative;
    width: 100%;
    img {
      position: absolute;

      width: 1.5rem;
    }
    span {
      padding-left: 3rem;
      font-size: 1.3rem;
      font-weight: 500;
    }
  }
  .arrow-icon {
    height: 1.5rem;
    width: auto;
    position: absolute;
    top: calc(50% - 0.75rem);
    right: 0;
    left: auto;
  }
}
@media (min-width: 1023px) {
  .categories-container {
    padding: 2rem;
    a {
      text-align: center;
    }
    .arrow-icon {
      display: none;
    }
  }
}
</style>
