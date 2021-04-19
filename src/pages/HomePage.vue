<template>
  <section class="main-section">
    <row class="is-background-white">
      <a href="#">
        <img src="@/assets/ic/black/ic_categories.png" alt="shopping icon" />
        <span>Shop All Categories</span></a
      >
    </row>
    <row class="nav-btns-container is-background-white">
      <NavBtn
        v-for="(category, index) in categories"
        :key="index"
        :text="category.text"
        :href="category.link"
        :icon="category.icon"
      ></NavBtn>
    </row>
    <row class="mobile-btns-row">
      <container class="mobile-btn-container">
        <a class="is-background-white" href="#">
          <img
            src="@/assets/ic/green/ic_line_style.png"
            alt="categories icon"
          />
        </a>
        <span>Categories</span>
      </container>
      <container class="mobile-btn-container">
        <a class="is-background-white" href="#">
          <img src="@/assets/ic/green/ic_search.png" alt="search icon" />
        </a>
        <span>Search</span>
      </container>
      <container class="mobile-btn-container">
        <a class="is-background-white" href="#">
          <img src="@/assets/ic/green/ic_scanner.png" alt="scanner icon" />
        </a>
        <span>Scan</span>
      </container>
    </row>
    <row class="deals-row">
      <a class="is-card" href="#"
        ><img src="@/assets/panel/deal.png" alt="todays deals"
      /></a>
    </row>
    <row class="members-row">
      <container class="is-card is-background-white">
        <img src="@/assets/img/platt-plus.png" alt="Platt Plus Membership" />
        <h2>Get Started Today</h2>
        <h3>Become a <span class="is-text-green">Platt Plus</span> Member.</h3>
        <a class="is-rounded-btn is-background-gray" href="#">Learn More</a>
      </container>
    </row>
    <row class="recently-viewed-row">
      <container class="is-card">
        <row class="card-header">
          <column>
            <span>Recently Viewed</span>
          </column>
          <column>
            <a class="is-text-green" href="#">View All</a>
          </column>
        </row>
        <row class="card-content">
          <a href="#"
            ><img src="@/assets/recent/11.png" alt="recent photo"
          /></a>
          <a href="#"
            ><img src="@/assets/recent/22.png" alt="recent photo"
          /></a>
          <a href="#"
            ><img src="@/assets/recent/22.png" alt="recent photo"
          /></a>
        </row>
      </container>
    </row>
    <row class="quick-links-row">
      <container class="is-card is-background-white">
        <a href="#">
          <img src="@/assets/img/super-tool-day.png" alt="Super Tool Day" />
          <span>Super Tool Day & Dynamic Data Day</span>
        </a>
      </container>
      <container class="is-card is-background-white">
        <a href="#">
          <img src="@/assets/img/ic_location_b.png" alt="Branch Locations" />
          <span>Branch Locations</span>
        </a>
      </container>
      <container class="is-card is-background-white">
        <a href="#">
          <img src="@/assets/img/ic_helpcenter.png" alt="Help Center" />
          <span>Help Center</span>
        </a>
      </container>
      <container class="is-card is-background-white">
        <a href="#">
          <img src="@/assets/img/ic_platt-u.png" alt="Platt University" />
          <span>Platt University</span>
        </a>
      </container>
    </row>
  </section>
</template>

<script>
import NavBtn from "@/components/NavBtn.vue";
import store from "../store";
export default {
  name: "HomePage",
  components: {
    NavBtn,
  },
  props: {},
  data() {
    return {
      categories: store.categories,
    };
  },
};
</script>

<style lang="scss" scoped>
.nav-btns-container {
  flex-direction: column;
  align-items: flex-start;

  .nav-btn {
    width: 100%;
  }
}
.mobile-btns-row {
  background-color: var(--gray);
}
.mobile-btn-container {
  width: auto;
  a {
    padding: 1.5rem;
    border-radius: 100px;
    margin-bottom: 1rem;
    box-shadow: 0px 2px 5px -1px rgb(0 0 0 / 30%);
    img {
      width: 2.2rem;
      height: auto;
    }
  }
}
.deals-row {
  a {
    width: 100%;
    height: auto;
    img {
      width: 100%;
      height: auto;
    }
  }
}
.recently-viewed-row {
  row {
    width: 100%;
  }
  .is-card {
    padding: 1rem;
    background-color: var(--white);
    .card-header {
      width: 100%;
      padding: 0;
    }
    .card-content {
      // overflow-x: scroll;
      a {
        display: inline-block;
      }
    }
  }
}
.quick-links-row {
  flex-wrap: wrap;
  .is-card {
    width: 48%;
    height: 15rem;
    margin-bottom: 1rem;
    a {
      display: flex;
      justify-content: space-between;
      height: 100%;
      align-items: center;
      flex-direction: column;
      padding: 1rem;
      text-align: center;
      img {
        width: 100%;
        height: auto;
      }
      span {
        display: flex;
        justify-content: center;
        align-items: center;
        height: 4rem;
        font-size: 1.2rem;
        font-weight: 600;
      }
    }
  }
}
</style>
