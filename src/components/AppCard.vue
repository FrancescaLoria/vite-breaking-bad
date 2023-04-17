<script>
export default {
  name: "AppCard",
  props: { img: String, title: String, type: String },
};
</script>

<template>
  <div class="ms_card text-center">
    <img :src="img" :alt="title" />
    <div class="name">{{ title }}</div>
    <div class="type">{{ type }}</div>
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
