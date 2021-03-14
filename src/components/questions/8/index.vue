<template>
  <div>
    <!-- FIXME: при переопределении слота, username не отображается -->
    <!--    FIXME: слот был неправильно переопределён (поле username выводилось, а объявлено не было)-->
    <slots-component-user>
      <span>Login: {{username}}</span>
    </slots-component-user>
  </div>
</template>

<script>
import SlotsComponentUser from "@/components/questions/8/SlotsComponentUser";

export default {
name: "SlotsComponent",
  components: {SlotsComponentUser},
  data: function () {
    return {
      username: 'NewVasyan'
    }
  }
}
</script>

<style scoped>
</style>
