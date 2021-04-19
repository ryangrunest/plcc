<template>
  <div class="nav-btn">
    <a v-bind:href="href">
      <div class="icon-container">
        <img v-bind:src="icon" v-bind:alt="text" />
      </div>
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
    index: Number,
  },
  created() {
    console.log(this.index);
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

    .icon-container {
      width: 1.7rem;
      height: 2rem;
      position: absolute;
      top: calc(50% - 0.85rem);
      left: 0;
      img {
        width: 100%;
        height: auto;
        position: absolute;
        margin: auto;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0;
      }
    }

    span {
      padding-left: 3rem;
      font-size: 1.2rem;
    }
    .arrow-icon {
      height: 1.2rem;
      width: auto;
      position: absolute;
      top: calc(50% - 0.6rem);
      right: 0;
      left: auto;
    }
  }
}
@media (min-width: 1023px) {
  .nav-btn {
    text-align: center;
    a {
      border: none;
      display: flex;
      align-items: center;
      padding: 1rem 0;
      padding-left: 30%;
      span {
        padding-left: 1rem;
      }
      .icon-container {
        position: relative;
      }
    }
    .arrow-icon {
      display: none;
    }
  }
}
</style>
