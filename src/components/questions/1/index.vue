<template>
<!-- TODO: При переключении типа логина, введенные значения должны очищаться || key look -->
  <div>
    <template v-if="loginType === 'phone'">
      <label>Phone</label>
      <input key="phone" placeholder="Enter your phone">
    </template>
    <template v-else>
      <label>Login</label>
      <input key="mail" placeholder="Enter your login">
    </template>
    <button @click="switchMethod">Change login type</button>
  </div>
</template>

<script>
export default {
  name: "LoginType",
  data() {
    return {
      loginType: 'phone'
    }
  },
  methods: {
    switchMethod() {
      this.loginType = this.loginType === 'phone' ? 'email' : 'phone';
    }
  },
}
</script>

<style scoped>

</style>
