<template>
  <footer class="is-background-darkgray">
    <div class="row">
      <div class="container">
        <a href="#" class="h3 is-text-white">Support Center</a>
        <a href="#" class="h3 is-text-white">800-25-Platt</a>
        <a href="#" class="h4 is-text-white">800-257-5288</a>
        <span class="h3 is-text-gray">4 a.m. - 12 a.m. (pst)</span>
        <span class="h3 mt-0 is-text-gray">7 Days a week</span>
        <button type="button">
          <img src="@/assets/ic/black/ic_chat.png" alt="live help icon" />
          <span>Live Help</span>
        </button>
      </div>
    </div>
    <div class="row footer-btns-row">
      <a class="is-text-white text-left" href="#">Contact Us</a>
      <a class="is-text-white text-center" href="#">What's New</a>
      <a class="is-text-white text-right" href="#">FAQ's</a>
    </div>
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
  height: 3rem;
  margin: 2rem 0;
  border-radius: 100px;
  position: relative;
  text-align: center;
  span {
    display: inline-block;
    font-size: 1.2rem;
    text-align: center;
  }
  img {
    position: absolute;
    left: 4rem;
    width: 1rem;
  }
}
.h3 {
  font-size: 1.5rem;
  font-weight: 500;
  margin-top: 1rem;

  &:last-of-type {
    margin-top: 0;
  }
}
.h4 {
  font-size: 1.1rem;
}
.footer-btns-row {
  padding: 2.5rem 2.5rem;
  padding-top: 1rem;
  a {
    font-size: 1.2rem;
    font-weight: 500;
    width: 33%;
  }
}
</style>
