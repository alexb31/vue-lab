<template lang="pug">
  #hours
    p(v-if="hours < 12") Good Morning
    p(v-if="hours >= 12 && hours < 18") Good Afternoon
    p(v-if="hours >= 18") Good Evening
    p it's {{hours}}
</template>

<script>
export default {
  name: "Hours",
  data() {
    return {
      hours: new Date().getHours()
    }
  }
}
</script>
