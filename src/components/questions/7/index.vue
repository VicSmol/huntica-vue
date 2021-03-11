<template>
    <div>
      <input v-model.trim="phone" class="phone" placeholder="phone" />
      <span v-if="error">Неправильно введен номер телефона</span>
    </div>
</template>

<script>
// TODO: реализовать валидацию входных данных свойства и валидацию input - тип телефон, вида +7(XXX)-XXX-XX-XX
//TODO: Сделал неправильно, т.к. не работал валидатор на prop value
export default {
  name: "PhoneValidation",
  props: {
    value: {
      type: String,
      default: '',
      required: true,
    },
  },
  data() {
    return {
      error: Boolean
    }
  },
  computed: {
    phone: {
      get() {
        return this.value
      },
      set(value) {
        const predicate = value.match(/^\+7\(\d{3}\)-\d{3}-\d{2}-\d{2}$/) !== null;

        this.value = predicate ? value : this.value
        this.error = !predicate
      }
    }
  },
}
</script>

<style scoped>
  .error {
    color: red
  }
</style>
