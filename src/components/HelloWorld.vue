<template>
  <section v-if="hasFruit">
    <h1>Fruits</h1>
    <ul>
      <li v-for="fruit in fruits"
          :key="fruit">{{ fruit }}
      </li>
    </ul>
  </section>
  <section>
    <h1>Reverse Fruits</h1>
    <ul>
      <li v-for="fruit in reverseFruits"
          :key="fruit">{{ fruit }}
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  data() {
    return {
      fruits: ["apple", "banana", "orange"]
    }
  },
  computed: {
    hasFruit() {
      return this.fruits.length > 2
    },
    reverseFruits() {
      return this.fruits.map(fruit => {
        return fruit.split('').reverse().join('')
      })
    }
  }
}
</script>