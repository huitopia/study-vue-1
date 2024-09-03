<template>
  <h1 @click="increase">{{ count }}</h1>
  <div v-if="count > 4">4보다 커야 보임</div>
  <ul>
    <li v-for="fruit in fruits"
        :key="fruit">
      {{ fruit }}
    </li>
  </ul>
</template>
<script>
export default {
  data() {
    return {
      count: 0,
      fruits: ["apple", "banana", "cherry"]
    }
  },
  methods: {
    increase() {
      this.count++;
    }
  }
}
</script>
<style>
h1 {
  font-size: 30px;
  color: royalblue;
}

ul li {
  font-size: 40px;
}
</style>