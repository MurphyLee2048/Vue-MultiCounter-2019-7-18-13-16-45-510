<template>
  <div>
    <button v-on:click="decrease">-</button>
    <span>{{count}}</span>
    <button v-on:click="increase">+</button>
  </div>
</template>

<script>
  export default {
    name: "Counter",
    methods: {
      increase() {
        this.count++;
      },
      decrease() {
        this.count--;
      }
    },
    data() {
      return {
        count: 0
      }
    }
  }
</script>

<style scoped>

</style>
