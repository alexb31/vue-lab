<template lang="pug">
  #bind
    button(v-bind:type="buttonType") Submit Bind
</template>

<script>
export default {
  data() {
    return {
      buttonType: "submit"
    }
  }
}
</script>
