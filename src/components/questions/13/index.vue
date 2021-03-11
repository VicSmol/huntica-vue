<template>
    <!-- TODO: реализовать указанный шаблон с помощью функции render() -->
    <!--  TODO: видимо нужно слот написать? и при вызове его переопределить?-->
    <div :class="{'active': isActive}">
      <slot><p> {{name}} </p></slot>
    </div>
</template>

<script>
export default {
  name: "RenderFunction",
  data() {
    return {
      isActive: true,
      name: 'Vasyan'
    }
  },
}
</script>

<style scoped>

</style>
