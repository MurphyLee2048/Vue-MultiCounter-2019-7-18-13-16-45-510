<template>
  <div>
    <input v-model.number="number" placeholder="CounterNumber">
    <Counter v-for="n in number"></Counter>
  </div>
</template>

<script>
  import Counter from "./Counter"

  export default {
    name: "CounterGroup",
    data() {
      return {
        number: 1
      }
    },
    components: {Counter}
  }
</script>

<style scoped>

</style>
