<template>
  <h1 @click="changeMessage">{{ msg }}</h1>
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
  watch: {
    msg(newMsg) {
      console.log("this.msg = newMsg", newMsg)
    },
    reverseMessage() {
      console.log("reverse: ", this.reverseMessage)
    }
  },
  methods: {
    changeMessage() {
      this.msg = "hi"
    }
  }
}
</script>
<style></style>