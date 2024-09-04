<template>
  <h1>{{ reverseMessage }}</h1>
</template>
<script>
export default {
  data() {
    return {
      msg: "hello computed"
    }
  },
  computed: {
    reverseMessage() {
      return this.msg.split('').reverse().join('')
    }
  }
}
</script>
<style></style>