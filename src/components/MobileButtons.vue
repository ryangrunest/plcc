<template>
  <div class="row mobile-btns-row">
    <div class="container mobile-btn-container">
      <a class="is-background-white" href="#">
        <img src="@/assets/ic/green/ic_line_style.png" alt="categories icon" />
      </a>
      <span>Categories</span>
    </div>
    <div class="container mobile-btn-container">
      <a class="is-background-white" href="#">
        <img src="@/assets/ic/green/ic_search.png" alt="search icon" />
      </a>
      <span>Search</span>
    </div>
    <div class="container mobile-btn-container">
      <a class="is-background-white" href="#">
        <img src="@/assets/ic/green/ic_scanner.png" alt="scanner icon" />
      </a>
      <span>Scan</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "MobileButtons",
  props: {},
};
</script>

<style lang="scss" scoped>
.mobile-btns-row {
  background-color: var(--gray);
  padding: 1.2rem 2rem;
}
.mobile-btn-container {
  width: auto;
  a {
    padding: 1.8rem;
    border-radius: 100px;
    margin-bottom: 1rem;
    box-shadow: 0px 2px 5px -1px rgb(0 0 0 / 30%);
    img {
      width: 2.2rem;
      height: auto;
    }
  }
}
</style>
