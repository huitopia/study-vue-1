<template>
  <button @click="add">ADD</button>
  <h1>{{ reverseMessage }}</h1>
</template>
<script>
export default {
  data() {
    return {
      // Getter & Setter
      msg: "hello computed"
    }
  },
  computed: {
    // Getter
    // reverseMessage() {
    //   return this.msg.split('').reverse().join('')
    // }
    // Getter & Setter
    reverseMessage: {
      get() {
        return this.msg.split('').reverse().join('')
      },
      set(newMsg) {
        this.msg = newMsg
      }
    }
  },
  methods: {
    add() {
      this.reverseMessage += "!?"
    }
  }
}
</script>
<style></style>