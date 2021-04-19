<template>
  <div class="nav-btn">
    <a v-bind:href="href">
      <img v-bind:src="icon" v-bind:alt="text" />
      <span>{{ text }}</span>
      <img
        class="arrow-icon"
        src="@/assets/ic/black/ic_arrow_forward.png"
        alt="arrow icon"
      />
    </a>
  </div>
</template>

<script>
export default {
  name: "NavBtn",
  props: {
    text: String,
    href: String,
    icon: String,
  },
};
</script>

<style scoped lang="scss">
.nav-btn {
  margin: 0 1rem;

  a {
    display: block;
    position: relative;
    padding: 1.5rem 0;
    border-top: 1px solid var(--lightgray);

    img {
      width: 1.5rem;
      position: absolute;
      left: 0;
      top: 38%;
    }

    span {
      padding-left: 2em;
      font-size: 1.5rem;
    }

    .arrow-icon {
      right: 0;
      left: auto;
    }
  }
}
</style>
