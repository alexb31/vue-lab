<template lang="pug">
  #computed
    h1 Computed properties
    p Sum of numbers: {{ numberTotal }}
    p {{ doubleValue }}
    button(v-on:click="A++") Add To A
    button(v-on:click="B++") Add To B
    p A - {{ A }}
    p B - {{ B }}
    p Age + A = {{addToA}}
    p Age + B = {{addToB}}
</template>

<script>
export default {
  data() {
    return {
      numbers: [1, 5, 9, 22],
      value: 11,
      age: 20,
      A: 0,
      B: 0
    };
  },
  methods: {
    // addToA() {
    //   console.log("A Changed");
    //   return this.A + this.age;
    // },
    // addToB() {
    //   console.log("B Changed");
    //   return this.B + this.age;
    // }
  },
  computed: {
    numberTotal: {
      get() {
        console.log("numberTotal");
        return this.numbers.reduce((sum, val) => sum + val);
      },
      set(newValue) {
        console.log("oldValue");
        const oldValue = this.numberTotal;
        console.log("difference");
        const difference = newValue - oldValue;
        this.numbers.push(difference);
      }
    },
    doubleValue() {
      console.log("Value Changed");
      return this.value * 2;
    },
    addToA() {
      console.log("A Changed");
      return this.A + this.age;
    },
    addToB() {
      console.log("B Changed");
      return this.B + this.age;
    }
  }
};
</script>