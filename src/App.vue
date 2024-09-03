<template>
  <h1 @click="increase">{{ count }}</h1>
  <div v-if="count > 4">4보다 커야 보임</div>
  <ul>
    <FruitList
        v-for="fruit in fruits"
        :key="fruit"
        :name="fruit">
      {{ fruit }}
    </FruitList>
  </ul>
</template>
<script>
import FruitList from "@/components/FruitList.vue";

export default {
  components: {
    // : FruitList 생략 가능
    FruitList
  },
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
  color: royalblue;
}

ul li {
  color: cadetblue;
}
</style>