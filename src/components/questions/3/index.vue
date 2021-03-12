<template>
<div>
  <ul>
    <!-- FIXME: Vue не рекомендует использовать одновременно v-for и v-if, необходимо внести изменения-->
    <li
        v-for="person in persons"
        :key="person.id"
    >
      {{ person.name }}
    </li>
  </ul>
</div>
</template>

<script>
export default {
  name: "UsersListVFor",
  data() {
    return {
      users: [
        {
          id: 1,
          name: 'Nagibator2005',
          isActive: true,
        },
        {
          id: 2,
          name: 'Nagibator2006',
          isActive: false,
        }
      ]
    }
  },
  computed: {
    persons: {
      get() {
        return this.users.filter(user => user.isActive);
      }
    }
  }
}
</script>

<style scoped>

</style>
