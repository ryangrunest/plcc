<template>
  <div class="row nav-btns-container is-background-white">
    <NavBtn
      v-for="(category, index) in categories"
      :key="index"
      :text="category.text"
      :href="category.link"
      :icon="category.icon"
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
</style>
