<template>
  <div>
    <input type="number" v-model.number="number" placeholder="CounterNumber">
    <Counter v-for="n in number" v-on:addAll="addAll"></Counter>
    <p>{{sum}}</p>
  </div>
</template>

<script>
  import Counter from "./Counter"

  export default {
    name: "CounterGroup",
    data() {
      return {
        number: 1,
        sum: 0
      }
    },
    methods: {
      addAll(count) {
        this.sum += count;
      }
    },
    components: {Counter}
  }
</script>

<style scoped>

</style>
