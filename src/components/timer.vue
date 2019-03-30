<template lang="pug">
  #timer
    button(:disabled="buttonDisabled") {{buttonDisabled}}
    p {{ seconds }} seconds have elapsed since you opened the page
</template>

<script>
export default {
  data() {
    return {
      seconds: 0,
      buttonDisabled: true
    }
  },
  created() {
    setInterval(() => {
      this.seconds++
      this.buttonDisabled = !this.buttonDisabled
    }, 1000);
  }
}
</script>
