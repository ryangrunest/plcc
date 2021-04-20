<template>
  <Header />
  <HomePage />
  <Footer />
</template>

<script>
import Header from "./components/Header.vue";
import HomePage from "./pages/HomePage.vue";
import Footer from "./components/Footer";

export default {
  name: "App",
  components: {
    Header,
    HomePage,
    Footer,
  },
};
</script>

<style lang="scss">
:root {
  --white: rgb(255, 255, 255);
  --black: rgb(0, 0, 0);
  --gray: rgb(240, 240, 240);
  --lightgray: rgb(195, 195, 195);
  --darkgray: rgba(117, 117, 117);
  --green: rgb(68, 147, 79);
}
* {
  margin: 0;
  padding: 0;
  font-size: 15px;
  color: var(--black);

  &:focus {
    outline: 3px solid var(--green);
  }
  .mt-0 {
    margin-top: 0;
  }
  .text-left {
    text-align: left;
  }
  .text-center {
    text-align: center;
  }
  .text-right {
    text-align: right;
  }
  .is-card {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    box-shadow: 0px 2px 7px -1px rgb(0 0 0 / 60%);
  }
  .is-background-green {
    background-color: var(--green);
  }
  .is-background-gray {
    background-color: var(--gray);
  }
  .is-background-darkgray {
    background-color: var(--darkgray);
  }
  .is-background-white {
    background-color: var(--white);
  }
  .is-text-green {
    color: var(--green);
  }
  .is-text-white {
    color: var(--white);
  }
  .is-text-gray {
    color: var(--gray);
  }
}
a,
button {
  text-decoration: none;
  &:hover {
    cursor: pointer;
  }
}

button,
input,
.is-rounded-btn {
  transition: 0.6s all cubic-bezier(0.2, 1.23, 0.84, 0.71);
  &:hover,
  &:active {
    box-shadow: 0px 3px 10px 3px rgb(0 0 0 / 30%);
  }
}
button,
.is-rounded-btn {
  border: none;
  padding: 0.6rem 1rem;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 100px;

  img {
    padding-right: 1rem;
  }
}
input {
  border: none;
  border-radius: 3px;
}
.row {
  display: flex;
  justify-content: space-between;
  align-content: center;
  align-items: center;
  flex-wrap: wrap;
  padding: 1.2rem 1rem;
  padding-bottom: 0;

  .column {
    display: flex;
    justify-content: flex-start;
    align-items: center;
    flex-wrap: wrap;

    &:last-of-type {
      justify-content: flex-end;
    }
  }
}
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  width: 100%;
  height: 100%;
}

#app {
  background-color: var(--gray);
  margin-bottom: 2.5rem;
  font-family: "Helvetica Neue", sans-serif;
}

@media (min-width: 1023px) {
  #app {
    margin-bottom: 0;
  }
}

@media (min-width: 1439px) {
  * {
    font-size: 35px;
  }
}
</style>
