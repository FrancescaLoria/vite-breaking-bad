<script>
export default {
  name: "AppCard",
};
</script>

<template>
  <div class="ms_card text-center">
    <img src="https://images.ygoprodeck.com/images/cards/34541863.jpg" alt="" />
    <div class="name">TITOLO CARTA</div>
    <div class="type">TIPO DI CARTA</div>
  </div>
</template>

<style scoped lang="scss">
.ms_card {
  img {
    width: 100%;
    object-fit: cover;
  }
}
</style>
