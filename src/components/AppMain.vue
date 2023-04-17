<script>
import AppCard from "./AppCard.vue";
import axios from "axios";
export default {
  name: "AppMain",
  data() {
    return {
      cardsArray: [],
    };
  },
  components: {
    AppCard,
  },
  beforeCreate() {
    axios
      .get("https://db.ygoprodeck.com/api/v7/cardinfo.php?num=20&offset=0")
      .then((resp) => {
        const myData = resp.data.data;
        this.cardsArray = myData;
      });
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
          <div class="col" v-for="(card, index) in cardsArray" :key="index">
            <AppCard
              :img="card.card_images[0].image_url"
              :title="card.name"
              :type="card.type"
            />
          </div>
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
