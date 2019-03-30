<template lang="pug">
  #loop
    ul
      li(v-for="(rent, city) in averageRent")
        p The rent of {{ city }} is ${{ rent }}
</template>

<script>
export default {
  data() {
    return {
      averageRent: {
        paris: 5120,
        london: 1690,
        dublin: 4721
      }
    }
  }
}
</script>
