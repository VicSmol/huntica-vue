<template>
  <!-- TODO: сделать компонент безопасным для использования и написать unit тесты с помощью Jest -->
  <!--  TODO: суть задания понимаю, но в силу малой практики с jest (тесты писал в проекте с nestjs), нужно отдельно вникать как что подключается и пишется-->
  <div>
    <user-component v-model="user"></user-component>
    <button @click="fetchUser">fetch user</button>
  </div>
</template>

<script>
import {asyncFetchUser} from "@/components/questions/12/helpers/asyncFetchUser";
import UserComponent from "./UserComponent";

export default {
  name: "ComponentForTest",
  components: {UserComponent},
  data() {
    return {
      user: null,
    }
  },
  methods: {
    async fetchUser() {
      this.user = await asyncFetchUser()
    }
  },
}
</script>

<style scoped>

</style>
