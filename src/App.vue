<script>
import NavComponent from "./components/NavComponent.vue";
export default{
  components: {
    NavComponent,
  },
}
</script>

<template>

    <div>
      <NavComponent />
      <RouterView />

    </div>

</template>

<style scoped>

</style>
