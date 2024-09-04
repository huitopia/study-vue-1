<template>
  <section>
    <h1></h1>
    <ul>
      <li v-for="world in helloWorld"
          :key="world">{{ world }}
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  data() {
    return {
      helloWorld: ["apple", "banana", "orange"]
    }
  }
}
</script>