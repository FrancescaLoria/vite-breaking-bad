<script>
export default {
  name: "SearchBar",
  emits: ["filterCard"],
  data() {
    return {
      statusOptions: ["Alien", "Ally of Justice", "Ancient Gear"],
    };
  },
};
</script>

<template>
  <div class="ms_cont mb-4">
    <select
      name="status"
      id="status"
      @change="$emit('filterCard', $event.target.value)"
    >
      <option value="All">All</option>
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
