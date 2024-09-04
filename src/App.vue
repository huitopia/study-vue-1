<template>
  <h1
      @click="activate"
      :class="{active: isActive}"
  >Hello({{ isActive }})</h1>
</template>
<script>
export default {
  data() {
    return {
      isActive: false
    }
  },
  methods: {
    activate() {
      this.isActive = true
    }
  }
}
</script>

<style scoped>
.active {
  color: red;
}
</style>