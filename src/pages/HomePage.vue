<template>
  <section class="main-section">
    <row class="is-background-white categories-container">
      <a href="#">
        <img src="@/assets/ic/black/ic_categories.png" alt="shopping icon" />
        <span>Shop All Categories</span>
        <img
          class="arrow-icon"
          src="@/assets/ic/black/ic_arrow_forward.png"
          alt="arrow icon"
      /></a>
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
    <MobileButtons />
    <Deals />
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
    <row class="app-download-row">
      <container class="is-card is-background-white">
        <a href="#">
          <!-- <img
            src="@/assets/panel/app-get-banner.png"
            alt="download the mobile app"
          /> -->
          <div class="bg-img"></div>
          <span>Shop Better, download the Platt App today</span>
        </a>
      </container>
    </row>
  </section>
</template>

<script>
import NavBtn from "@/components/NavBtn.vue";
import MobileButtons from "@/components/MobileButtons.vue";
import Deals from "@/components/Deals.vue";
import store from "../store";
export default {
  name: "HomePage",
  components: {
    NavBtn,
    MobileButtons,
    Deals,
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
.categories-container {
  padding: 2.2rem 2rem;
  position: relative;
  a {
    position: relative;
    width: 100%;
    img {
      position: absolute;

      width: 1.5rem;
    }
    span {
      padding-left: 3rem;
      font-size: 1.3rem;
      font-weight: 500;
    }
  }
  .arrow-icon {
    height: 1.5rem;
    width: auto;
    position: absolute;
    top: calc(50% - 0.75rem);
    right: 0;
    left: auto;
  }
}
.nav-btns-container {
  flex-direction: column;
  align-items: flex-start;
  padding: 0 2rem;
  padding-bottom: 0.8rem;

  .nav-btn {
    width: 100%;
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
  margin-bottom: -1rem;
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
.app-download-row {
  padding-bottom: 1.5rem;
  a {
    width: 100%;
  }
  .bg-img {
    height: 10rem;
    background-repeat: no-repeat;
    background-position: right;
    background-size: auto 100%;
    background-image: url("/assets/panel/app-get-banner.png");
  }
  span {
    display: block;
    text-align: center;
    width: 100%;
    padding: 1rem 0;
    font-size: 1.2rem;
    font-weight: 500;
  }
}
</style>
