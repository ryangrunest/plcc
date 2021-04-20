<template>
  <header class="is-background-green" id="header">
    <div class="navbar">
      <div class="row navbar-main-row">
        <div class="column">
          <div class="navbar-brand">
            <img src="@/assets/img/logo.png" alt="Platt Logo" />
          </div>
        </div>
        <div class="column nav-links-column">
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
        </div>
      </div>
      <div class="row navbar-search-row">
        <input
          @input="inputHandler"
          :value="searchField"
          placeholder="What are you looking for?"
          type="text"
        />
        <img src="@/assets/ic/black/ic_search.png" alt="search icon" />
        <div
          v-if="comparedCharacters.length > 0"
          class="intelli-search-container"
        >
          <ul class="intelli-search">
            <li
              @click="clickHandler"
              v-for="(character, index) in comparedCharacters"
              :key="index"
            >
              {{ character }}
            </li>
          </ul>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
import axios from "axios";
export default {
  name: "Header",
  props: {},
  data() {
    return {
      characters: [],
      comparedCharacters: [],
      searchField: "",
    };
  },
  created() {
    this.retrieveApiData();
  },
  methods: {
    retrieveApiData() {
      try {
        const config = {
          method: "GET",
          url: "https://swapi.dev/api/people/",
        };
        axios(config).then((response) => {
          this.characters = response.data.results;
        });
      } catch (err) {
        console.warn("error retrieving data for api", err);
        return;
      }
    },
    inputHandler(event) {
      try {
        this.searchField = event.target.value.toLowerCase();
        this.comparedCharacters = [];
        //compare characters
        this.characters.forEach((character) => {
          let characterName = character.name.toLowerCase();
          if (
            characterName.includes(this.searchField) &&
            this.searchField.length > 0
          ) {
            this.comparedCharacters.push(character.name);
          }
        });
      } catch (err) {
        console.warn("error with search field input handler", err);
        return;
      }
    },
    clickHandler(event) {
      try {
        event.preventDefault();
        this.searchField = event.target.innerText;
        this.comparedCharacters = [];
      } catch (err) {
        console.warn("error with search dropdown list click event", err);
        return;
      }
    },
  },
};
</script>

<style scoped lang="scss">
input {
  width: 100%;
  padding: 1.2rem 1rem;
  z-index: 20;
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
    z-index: 25;
  }
}
.navbar-brand {
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
  a {
    margin-left: 1.3rem;
  }
  :first-child {
    margin-left: 0;
  }

  img {
    width: 1.6rem;
    height: auto;
  }
}
.intelli-search-container {
  position: absolute;
  top: 4.4rem;
  width: calc(100% - 6rem);
  border-top: 1px solid var(--lightgray);
  box-shadow: 0px 0px 9px 0px rgb(0 0 0 / 30%);
  display: flex;
  padding: 1rem 1rem;
  z-index: 10;
  background-color: var(--white);
  ul {
    list-style: none;
    li {
      line-height: 2rem;
      font-size: 1.1rem;
      color: var(--darkgray);
      &:hover {
        cursor: pointer;
      }
      &:hover,
      &:active {
        color: var(--black);
      }
    }
  }
}

@media (min-width: 1023px) {
  .navbar-main-row {
    padding: 2rem;
    padding-bottom: 0;
  }
}
</style>
