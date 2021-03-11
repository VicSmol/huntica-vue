<template>
  <div>
    <h1>Step 2</h1>
    <input v-model="text" />
  </div>
</template>

<script>
export default {
  name: "StepsComponentTwo",
  props: {
    value: {
      type: String,
      default: ''
    }
  },
  computed: {
    text: {
      get() {
        return this.value
      },
      set(value) {
        this.$emit('input', value);
      }
    }
  }
}
</script>

<style scoped>

</style>
