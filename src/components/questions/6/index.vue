<template>
  <div>
    <!-- TODO: при нажатии на кнопку "Enter Email" инпут должен появляться с фокусом на нем-->
    <input v-if="showEmailInput" ref="email">
    <button @click="show">Enter Email</button>
  </div>
</template>

<script>
export default {
  name: "InputFocus",
  data() {
    return {
      showEmailInput: false
    }
  },
  methods: {
    show() {
      this.showEmailInput = true

      this.$nextTick(() => this.$refs.email.focus())
    }
  }
}
</script>

<style scoped>

</style>
