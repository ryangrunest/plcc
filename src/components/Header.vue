<template>
  <header class="is-background-green" id="header">
    <navbar>
      <row>
        <row>
          <navbar-brand>
            <img src="@/assets/img/logo.png" alt="Platt Logo" />
          </navbar-brand>
        </row>
        <row>
          <a href="#"
            ><img src="@/assets/ic/white/ic_search.png" alt="search icon"
          /></a>
          <a href="#"
            ><img src="@/assets/ic/white/ic_shopping_cart.png" alt="cart icon"
          /></a>
          <a href="#"
            ><img src="@/assets/ic/white/ic_person.png" alt="profile icon"
          /></a>
          <a href="#"
            ><img src="@/assets/ic/white/ic_menu.png" alt="menu icon"
          /></a>
        </row>
      </row>
      <row>
        <input placeholder="What are you looking for?" type="text" />
      </row>
    </navbar>
  </header>
</template>

<script>
export default {
  name: "Header",
  props: {},
};
</script>

<style scoped lang="scss">
input {
  width: 100%;
  padding: 1rem;
}
</style>
