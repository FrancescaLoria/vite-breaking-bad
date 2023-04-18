<script>
export default {
  name: "SearchBar",
  data() {
    return {
      statusOptions: ["Alien", "Ally of Justice", "Ancient Gear"],
    };
  },
};
</script>

<template>
  <div class="ms_cont mb-4">
    <select name="status" id="status">
      <option value="">All</option>
      <option :value="status" v-for="status in statusOptions">
        {{ status }}
      </option>
    </select>
  </div>
</template>

<style scoped lang="scss">
.ms_cont {
  width: 87%;
  margin: 0 auto;
}
</style>
