<template>
  <div v-if="user">
    Username: {{ user.username }}<br>
  </div>
</template>

<script>
  export default {
    name: "UserComponent",
    props: {
      value: {}
    },
    computed: {
      user: {
        get() {
          return this.value
        },
        set(value) {
          this.value = value
        }
      }
    }
  }
</script>

<style scoped>

</style>