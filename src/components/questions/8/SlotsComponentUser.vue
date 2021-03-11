<template>
  <div>
    <slot name="user" v-bind="{username}">
      Username: {{username}}
    </slot>
  </div>
</template>

<script>
export default {
name: "SlotsComponentUser",
  data() {
    return {
      username: 'Vasyan'
    }
  },
}
</script>

<style scoped>

</style>
