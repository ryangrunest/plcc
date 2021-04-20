<template>
  <div class="row nav-btns-container is-background-white">
    <NavBtn
      v-for="(category, index) in categories"
      :key="index"
      :text="category.text"
      :href="category.link"
      :icon="category.icon"
      :index="index"
    ></NavBtn>
  </div>
</template>

<script>
import NavBtn from "@/components/NavBtn.vue";
import store from "@/store.js";
export default {
  name: "Nav",
  props: {},
  components: {
    NavBtn,
  },
  data() {
    return {
      categories: store.categories,
    };
  },
};
</script>

<style lang="scss" scoped>
.nav-btns-container {
  flex-direction: column;
  align-items: flex-start;
  padding: 0 2rem;
  padding-bottom: 0.8rem;

  .nav-btn {
    width: 100%;
  }
}
@media (min-width: 1023px) {
  .nav-btns-container {
    grid-column: 1 / 5;
    grid-row: 2;
    flex-direction: row;
    flex-wrap: wrap;
    padding: 0;
    border-bottom: 1px solid var(--lightgray);
    .nav-btn {
      width: 33.3333333%;
      margin: 0;
      box-sizing: border-box;
      border-top: 1px solid var(--lightgray);
      border-right: 1px solid var(--lightgray);
    }
  }
}
</style>
