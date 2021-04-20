<template>
  <section class="main-section">
    <Categories />
    <Nav />
    <MobileButtons />
    <Deals />
    <Members />
    <Recents />
    <QuickLinks />
    <AppDownload />
  </section>
</template>

<script>
import AppDownload from "@/components/AppDownload.vue";
import Categories from "@/components/Categories.vue";
import Deals from "@/components/Deals.vue";
import MobileButtons from "@/components/MobileButtons.vue";
import Members from "@/components/Members.vue";
import Nav from "@/components/Nav.vue";
import QuickLinks from "@/components/QuickLinks.vue";
import Recents from "@/components/Recents.vue";

export default {
  name: "HomePage",
  components: {
    AppDownload,
    Categories,
    Deals,
    MobileButtons,
    Members,
    Nav,
    QuickLinks,
    Recents,
  },
  props: {},
};
</script>

<style lang="scss" scoped>
@media (min-width: 1023px) {
  .main-section {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;
    column-gap: 1rem;
    align-items: center;
    align-content: start;
    justify-content: center;
  }
}
</style>
