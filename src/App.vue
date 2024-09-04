<template>
  <h1
      :style="{color, fontSize}"
      @click="changeStyle"
  >Hello</h1>
</template>
<script>
export default {
  data() {
    return {
      color: "blue",
      fontSize: "30px"
    }
  }
}
</script>
<style>

</style>