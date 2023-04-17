<script>
import AppCard from "./AppCard.vue";
export default {
  name: "AppMain",
  components: {
    AppCard,
  },
};
</script>

<template>
  <main class="pt-5">
    <div class="container">
      <div class="card-container pt-5">
        <div class="card-number">
          <div class="number py-3 ms-2">Found 20 cards</div>
        </div>
        <div class="row row-cols-5">
          <div class="col"><AppCard /></div>
          <div class="col"><AppCard /></div>
          <div class="col"><AppCard /></div>
          <div class="col"><AppCard /></div>
          <div class="col"><AppCard /></div>
        </div>
      </div>
    </div>
  </main>
</template>

<style scoped lang="scss">
@import "../style/varaibles";
main {
  background-color: $main_color;

  .container {
    background-color: white;
  }

  .card-container {
    width: 90%;
    margin: 0 auto;
  }

  .card-number {
    background-color: #212529;
    color: white;
    font-size: 13px;
  }
}
</style>
