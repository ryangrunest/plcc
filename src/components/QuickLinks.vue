<template>
  <div class="row quick-links-row">
    <div class="container is-card is-background-white">
      <a href="#">
        <img src="@/assets/img/super-tool-day.png" alt="Super Tool Day" />
        <span>Super Tool Day & Dynamic Data Day</span>
      </a>
    </div>
    <div class="container is-card is-background-white">
      <a href="#">
        <img src="@/assets/img/ic_location_b.png" alt="Branch Locations" />
        <span>Branch Locations</span>
      </a>
    </div>
    <div class="container is-card is-background-white">
      <a href="#">
        <img src="@/assets/img/ic_helpcenter.png" alt="Help Center" />
        <span>Help Center</span>
      </a>
    </div>
    <div class="container is-card is-background-white">
      <a href="#">
        <img src="@/assets/img/ic_platt-u.png" alt="Platt University" />
        <span>Platt University</span>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: "QuickLinks",
  props: {},
};
</script>

<style scoped lang="scss">
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
</style>
