<template lang="pug">
  #twoWayBind
    input(:type="inputProperty" v-model="inputText")
    p input Text: {{inputText}}
    <label><input type="radio" v-model="value" value="one"> One</label>
    <label><input type="radio" v-model="value" value="two"> Two</label>
    <label><input type="radio" v-model="value" value="three"> Three</label>
    p The value is {{ value }}
</template>

<script>
export default {
  data() {
    return {
      inputProperty: 'text',
      inputText: "Default Value",
      value: 0
    }
  }
}
</script>
