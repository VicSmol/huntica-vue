<template>
<!-- TODO: При переключении типа логина, введенные значения должны очищаться -->
  <div>
    <template v-if="loginType === 'phone'">
      <label>Phone</label>
      <input v-model="text" placeholder="Enter your phone">
    </template>
    <template v-else>
      <label>Login</label>
      <input v-model="text" placeholder="Enter your login">
    </template>
    <button @click="switchMethod">Change login type</button>
  </div>
</template>

<script>
export default {
  name: "LoginType",
  data() {
    return {
      loginType: 'phone',
      text: ''
    }
  },
  methods: {
    switchMethod() {
      this.loginType = this.loginType === 'phone' ? 'email' : 'phone';

      this.text = ''
    }
  },
}
</script>

<style scoped>

</style>
