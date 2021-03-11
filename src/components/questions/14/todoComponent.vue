<template>
  <div class="todo-list">
    <div
        v-for="{ id, title, completed } in todos"
        :key="id"
        class="todo-list__task"
    >
        <span :class="{ 'todo-list__task--completed': completed }">
          {{ title }}
        </span>
    </div>
  </div>
</template>

<script>
  export default {
    name: "todoComponent",
    props: {
      value: {
        type: Array,
        default: null
      }
    },
    computed: {
      todos: {
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