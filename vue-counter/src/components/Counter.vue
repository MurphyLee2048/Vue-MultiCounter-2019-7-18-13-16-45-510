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
        this.$emit('addAll', 1);
      },
      decrease() {
        this.count--;
        this.$emit('addAll', -1);
      },
    },
    data() {
      return {
        count: 0
      }
    },
    beforeDestroy: function () {
      this.$emit('addAll', this.count*(-1));
    }
  }
</script>

<style scoped>

</style>
