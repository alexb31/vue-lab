<template lang="pug">
  #this
    p The sum of positive numbers is {{ getPositiveNumbersSum() }}
</template>

<script>
export default {
  data() {
    return {
      numbers: [-5, -4, 9, 9, 5, 1]
    };
  },
  methods: {
    getPositiveNumbers() {
      return this.numbers.filter(number => number >= 0);
    },
    getPositiveNumbersSum() {
      return this.getPositiveNumbers().reduce((sum, val) => sum + val);
    }
  }
};
</script>