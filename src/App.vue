<template>
  <h1>{{ msg }}</h1>
  <h1>{{ reverseMessage }}</h1>
</template>
<script>
export default {
  data() {
    return {
      // Getter & Setter
      msg: "Hello"
    }
  },
  computed: {
    reverseMessage() {
      return this.msg.split('').reverse().join('')
    }
  },
  methods: {
    changeMessage() {
      this.msg = "!!"
    }
  }
}
</script>
<style></style>