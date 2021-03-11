<template>
  <input type="text" v-model="text">
</template>

<script>
export default {
  name: "CustomInput",
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

      set (value) {
        this.$emit('input', value)
      }
    }
  }
}
</script>

<style scoped>
</style>
