<template lang="pug">
  #dogs
    p The first dog is {{ dogs[0] }}
    p The dogs name are {{ dogs }}
    ul
      li(v-for="(dog, i) in dogs") {{ i }} {{ dog }}
</template>

<script>
export default {
  data() {
    return {
      dogs: ["Rex", "Lassie", "Milou", "Snowy"]
    }
  }
}
</script>
