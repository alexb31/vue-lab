<template lang="pug">
  #methods
    p Current status: {{ statusFromId(status) }}
    ul
      li(v-for="number in filterPositive(numbers)") {{ number }}
</template>

<script>
export default {
  data() {
    return {
      status: 1,
      numbers: [-5, -4, 8, 9, 5, 1]
    }
  },
  methods: {
    filterPositive(numbers) {
      return numbers.filter((number) => number >= 0);
    },
    statusFromId(id) {
      const status = ({
        0: "Asleep",
        1: "Jerking",
        2: "working"
      })[id]

      return status || 'Unknow Pleasures' + id;
    }
  }
}
</script>
