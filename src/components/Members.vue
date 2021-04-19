<template>
  <div class="row members-row">
    <div class="container is-card is-background-white">
      <img src="@/assets/img/platt-plus.png" alt="Platt Plus Membership" />
      <div class="text-container">
        <h2>Get Started Today</h2>
        <h3>Become a <span class="is-text-green">Platt Plus</span> Member.</h3>
        <a class="is-rounded-btn is-background-gray" href="#">Learn More</a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Members",
  props: {},
};
</script>

<style scoped lang="scss">
.container {
  padding: 2rem;
}
img {
  width: 100%;
  max-width: 100%;
  height: auto;
}
.text-container {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  margin: 2rem 0;
  h2 {
    font-size: 1.5rem;
  }
  h3 {
    font-size: 1.3rem;
    span {
      font-size: inherit;
    }
  }
  a {
    padding: 1rem 0;
    width: 100%;
    margin: 1rem 0;
    font-size: 1.2rem;
  }
}
</style>
