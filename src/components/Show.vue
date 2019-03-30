<template lang="pug">
  #show
    div(v-if="isLoggedIn") EXCELLENT
    div(v-else-if="isLoginDisabled") NOT
    div(v-else) WE'RE NOT WORTH IT
</template>

<script>
export default {
  data() {
    return {
      msg: "Hello World!",
      isLoggedIn: false,
      isLoginDisabled: false
    }
  }
}
</script>
