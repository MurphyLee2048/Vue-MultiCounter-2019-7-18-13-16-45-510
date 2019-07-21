<template>
  <div>
    {{Sum}}
  </div>
</template>

<script>
  export default {
    name: "CounterSum",
    data() {
      return {
        Sum:0
      }
    },
    props: {
      Sum: Number
    }
  }
</script>

<style scoped>

</style>
