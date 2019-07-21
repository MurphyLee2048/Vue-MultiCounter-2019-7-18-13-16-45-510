<template>
  <div>
    <counter v-for+="n in counternumber"></counter>
  </div>
</template>

<script>
  export default {
    name: "CounterGroup",
    props: {

      counterNum: Number
    },
    beforeDestroy: function () {
      this.$emit('destory', this.count);
    },
  }
</script>

<style scoped>

</style>
