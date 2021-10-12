<template>
  <div>
    <Test :schools="schools" />
    
  </div>
</template>

<script>
export default {
  data() {
    return {
      schools: null,
    };
  },
  async fetch() {
    this.schools = await this.$axios.$get(
      "http://universities.hipolabs.com/search?country=Turkey"
    );
  },
};
</script>
