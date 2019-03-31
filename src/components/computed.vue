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
    hr
    p First Name : {{firstName}}
    p Last Name : {{lastName}}
    p
      | Full Name :
      input(type="text" v-model="fullName")
</template>

<script>
export default {
  data() {
    return {
      numbers: [1, 5, 9, 22],
      value: 11,
      age: 20,
      A: 0,
      B: 0,
      firstName: "Jotaro",
      lastName: "Kujo"
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
        const oldValue = this.numberTotal;
        console.log("oldValue : " + oldValue);
        console.log("difference");
        const difference = newValue - oldValue;
        console.log("difference : " + difference);
        this.numbers.push(difference);
      }
    },
    fullName: {
      get: function() {
        return this.firstName + " " + this.lastName;
      },
      set: function(value) {
        let parts = value.split(" ");
        this.firstName = parts[0];
        this.lastName = parts[1];
        console.log(value);
      }
    },
    newValue() {
      return (this.numberTotal += 55);
    },
    doubleValue() {
      console.log("Value Changed");
      return this.value * 2;
    },
    addToA() {
      return this.A + this.age;
    },
    addToB() {
      return this.B + this.age;
    }
  }
};
</script>