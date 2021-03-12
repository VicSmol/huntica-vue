<template>
  <div>
    <!-- TODO: при нажатии на кнопку "Enter Email" инпут должен появляться с фокусом на нем-->
    <input v-if="showEmailInput" v-focus >
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
    }
  },
  directives: {
    focus: {
      inserted: function (element) {
        element.focus();
      }
    }
  }
}
</script>

<style scoped>
</style>