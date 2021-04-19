<template>
  <section class="main-section">
    <row>
      <a href="#">
        <img src="@/assets/ic/black/ic_categories.png" alt="shopping icon" />
        <span>Shop All Categories</span></a
      >
    </row>
    <div class="nav-btns-container">
      <NavBtn
        v-for="(category, index) in categories"
        :key="index"
        :text="category.text"
        :href="category.link"
        :icon="category.icon"
      ></NavBtn>
    </div>
  </section>
</template>

<script>
import NavBtn from "@/components/NavBtn.vue";
import store from "../store";
export default {
  name: "HomePage",
  components: {
    NavBtn,
  },
  props: {},
  data() {
    return {
      categories: store.categories,
    };
  },
};
</script>

<style lang="scss" scoped></style>
