<script>
export default {
  name: "AppHeader",
};
</script>

<template>
  <header>
    <div class="container-fluid d-flex align-items-center py-3">
      <div class="logo">
        <img src="../assets/img/logo.png" alt="" />
      </div>
      <div class="title mx-3">
        <h1>Yu-Gi-Oh Api</h1>
      </div>
    </div>
  </header>
</template>

<style scoped lang="scss">
header {
  height: 100px;

  img {
    width: 69px;
    object-fit: cover;
  }
}
</style>
