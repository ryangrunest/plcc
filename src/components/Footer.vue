<template>
  <footer class="is-background-darkgray">
    <row>
      <container>
        <h3 class="is-text-white">Support Center</h3>
        <h3 class="is-text-white">800-25-Platt</h3>
        <h4 class="is-text-white">800-257-5288</h4>
        <h3 class="is-text-gray">4 a.m. - 12 a.m. (pst)</h3>
        <h3 class="is-text-gray">7 Days a week</h3>
        <button type="button">
          <img src="@/assets/ic/black/ic_chat.png" alt="live help icon" />
          <span>Live Help</span>
        </button>
      </container>
    </row>
    <row>
      <a class="is-text-white" href="#">Contact Us</a>
      <a class="is-text-white" href="#">What's New</a>
      <a class="is-text-white" href="#">FAQ's</a>
    </row>
  </footer>
</template>

<script>
export default {
  name: "Footer",
  props: {},
};
</script>

<style scoped lang="scss">
button {
  width: 17rem;
  margin: 2rem 0;
}
</style>
