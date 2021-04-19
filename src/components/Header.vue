<template>
  <header class="is-background-green" id="header">
    <navbar>
      <row>
        <column>
          <navbar-brand>
            <img src="@/assets/img/logo.png" alt="Platt Logo" />
          </navbar-brand>
        </column>
        <column class="nav-links-column">
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
        </column>
      </row>
      <row class="navbar-search-row">
        <input placeholder="What are you looking for?" type="text" />
        <img src="@/assets/ic/black/ic_search.png" alt="search icon" />
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
  padding: 1.2rem 1rem;
}
.navbar-search-row {
  padding: 2rem;
  padding-top: 1rem;
  position: relative;
  img {
    height: 1.5rem;
    position: absolute;
    top: calc(50% - 1.15rem);
    right: 3rem;
  }
}
navbar-brand {
  max-width: 50%;
  img {
    height: 2rem;
    width: auto;
  }
}
.nav-links-column {
  width: 100%;
  max-width: 50%;
  display: flex;
  justify-content: space-between;
  img {
    width: 1.6rem;
    height: auto;
  }
}
</style>
