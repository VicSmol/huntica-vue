<template>
  <div>
    <input v-model.trim="phone">
    <br><br>
    <phone-validation :value="phone"></phone-validation>
  </div>
</template>

<script>
// TODO: реализовать валидацию входных данных свойства и валидацию input - тип телефон, вида +7(XXX)-XXX-XX-XX

import PhoneValidation from "./PhoneValidation";

export default {
  name: "PhoneCheck",
  components: {PhoneValidation},
  data() {
    return {
      phone: ''
    }
  }
}
</script>

<style scoped>
</style>
