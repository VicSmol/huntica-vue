<template>
  <div>
    <span v-show="errorMsg">{{ errorMsg }}</span>
  </div>
</template>

<script>
  export default {
    name: "PhoneValidation",
    props: {
      value: {
        type: String,
        default: '',
        validator: value => value.match(/^\+7\(\d{3}\)-\d{3}-\d{2}-\d{2}$/) !== null
      }
    },
    data() {
      return {
        errorMsg: ''
      }
    },
    computed: {
      phone: {
        get() {
          return this.value
        }
      }
    },
    watch: {
      phone: function () {
        this.errorMsg = this.phone.match(/^\+7\(\d{3}\)-\d{3}-\d{2}-\d{2}$/) === null
          ? "Неправильно введен номер телефона"
          : ''
      }
    }
  }
</script>

<style scoped>
  .error {
    color: red
  }
</style>