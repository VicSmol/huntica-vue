<template>
  <div>
    <!-- FIXME: при нажатии на кнопку send форма отправляется по старому адресу  || рендеринг компонентов-->
    <form ref="form" :action="action">
      <input placeholder="Enter email" :key="action" />
    </form>
    <button @click="submit">Send</button>
  </div>
</template>

<script>
export default {
  name: "RefComponent",
  data() {
    return {
      action: 'https://example.com'
    }
  },
  methods: {
    async submit() {
      this.action = 'https://test.com';

      await this.$nextTick();

      this.$refs.form.submit();
    }
  }
}
</script>

<style scoped>

</style>
